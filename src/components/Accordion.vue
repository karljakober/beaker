<template>
  <div
    class="accordion"
    :class="[ accordionClasses ]">

    <div
      class="accordion__toggle"
      @click="toggleAccordion">
      <span v-show="defaultOpen">{{ openedTitle }}</span>
      <span v-show="!defaultOpen">{{ closedTitle }}</span>
    </div>

    <div class="accordion__menu">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({})
export default class Accordion extends Vue {
  @Prop()
  isOpen!: boolean;

  @Prop()
  noBorder!: boolean;

  @Prop()
  openedTitle!: string;

  @Prop()
  closedTitle!: string;

  defaultOpen = false;
  defaultBorder = false;

  created() {
    this.defaultOpen = this.isOpen;
    this.defaultBorder = this.noBorder;
  }

  toggleAccordion(event: any) {
    let menu = event.target.nextElementSibling,
      menuContent;

    // Check if accordion was toggled by title
    if (event.target.nodeName === "SPAN") {
      menu = event.target.parentElement.nextElementSibling;
    }

    menuContent = menu.firstChild;
    this.defaultOpen = !this.defaultOpen;

    if (!this.defaultOpen) {
      menu.style.maxHeight = 0;
    } else {
      menu.style.maxHeight = `calc(${menuContent.scrollHeight}px + 16px`;
    }
  }

  get accordionClasses() {
    let classes = [];

    if (this.defaultBorder) {
      classes.push("accordion--no-border");
    }

    if (!this.defaultOpen) {
      classes.push("is-closed");
    }

    return classes.join(" ");
  }
}
</script>

<style lang="less" scoped>
@import "./../styles/Imports";

.accordions {
  .accordion {
    &:last-child {
      .margin-bottom(@0);
    }

    .accordion__menu {
      .transition();
    }
  }
}

.accordion {
  .radius();
  background-color: @day-bg;
  border: 1px solid @day-input-border;
  .margin-bottom(3);
  text-align: left;

  &.is-closed {
    .accordion__menu {
      max-height: 0;
      .padding-v-sides(@0);
    }

    .accordion__toggle {
      &:before {
        content: "\e957";
      }
    }
  }
}

.accordion--no-border {
  border: 0;
  background-color: transparent;

  .accordion__toggle {
    .padding(@0);
    padding-left: 24px;

    &:before {
      left: 0;
      top: 2px;
    }
  }

  .accordion__menu {
    .padding(@0);
    .padding-top();
  }
}

.accordion__toggle,
.accordion__menu {
  width: 100%;
}

.accordion__toggle {
  .weight(@medium);
  color: @day-title;
  position: relative;
  .padding(2);
  .padding-left(5);
  cursor: default;
  user-select: none;

  &:before {
    content: "\e958";
    color: @icon;
    border: none;
    position: absolute;
    left: 16px;
    height: 15px;
    width: 15px;
    line-height: 15px;
    background-color: @light-3;
    border-radius: 2px;
    text-align: center;
    top: 17px;
    font-size: 10px;
    font-family: "icomoon";
    font-weight: 900;
  }
}

.accordion__menu {
  .transition();
  overflow: hidden;
  .padding(2);
  .padding-top(@0);
}

.accordions {
  .accordion {
    &:last-child {
      margin-bottom: 0px;
    }
  }
}

.night,
.night-theme {
  .accordion {
    border-color: @night-input-border;
    background-color: @night-bg;
  }

  .accordion--no-border {
    background-color: transparent;
  }

  .accordion__toggle {
    color: @night-title;

    &:before {
      background-color: @dark-4;
    }
  }
}
</style>
