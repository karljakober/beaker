<template>
  <v-select
    :value="value"
    :options="options"
    :disabled="disabled"
    :clearable="false"
    :searchable="searchable"
    :multiple="multiple"
    :placeholder="placeholder"
    ></v-select>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import vSelect from "vue-select";
Vue.component("v-select", vSelect);

export default {
  name: "Selector",
  extends: vSelect,

  components: {
    vSelect
  }
};
</script>

<style lang="less">
@import "./../styles/Imports";

.v-select {
  font-family: "Roboto";
  background-color: @day-dropdown-bg;
  border-color: @day-dropdown-border;
  .radius();

  &.open {
    .open-indicator:before {
      transform: none;
    }
  }

  .dropdown-toggle {
    border: 0;
    .padding-h-sides();
    .padding-v-sides(@0);
    height: 32px;
  }

  .open-indicator:before {
    border: 0;
    transform: none;
    content: "\e996";
    font-family: "icomoon";
    color: @icon;
    height: auto;
    width: auto;
  }

  .form-control {
    padding: 0;
  }

  .vs__selected-options {
    .padding(@0);
  }

  .selected-tag {
    .margin(@0);
    .margin-right();
    color: @day-paragraph;
    .padding(@0);
    line-height: 32px;
    border: 0;
    font-family: "Roboto";
  }

  input[type="search"],
  input[type="search"]:focus {
    .margin(@0);
    font-size: 14px;
    font-family: "Roboto";
    .padding-h-sides(0);
  }

  .dropdown-menu {
    .padding(0);
    background-color: @day-dropdown-bg;
    border-color: @day-dropdown-border;
    .day-shadow();

    li {
      line-height: 32px;

      a {
        color: @day-paragraph;
        .padding-h-sides();
        .padding-v-sides(0);
        text-decoration: none;

        &:hover,
        &.active,
        &.highlight {
          background-color: @light-3;
          color: @day-title;
        }
      }
    }

    .active {
      a {
        background-color: @light-3;
      }
    }

    .highlight {
      a {
        background-color: @light-3;
        color: @day-title;
      }
    }
  }
}

.night,
.night-theme {
  .v-select {
    font-family: "Roboto";
    background-color: @night-dropdown-bg;
    border-color: @night-dropdown-border;

    .selected-tag {
      color: @night-paragraph;
    }

    .dropdown-menu {
      background-color: @night-dropdown-bg;
      border-color: @night-dropdown-border;
      .night-shadow();

      li {
        line-height: 32px;

        a {
          color: @night-paragraph;
          .padding-h-sides();
          .padding-v-sides(0);

          &:hover,
          &.active,
          &.highlight {
            background-color: @night-hover;
            color: @night-title;
          }
        }
      }

      .active {
        a {
          background-color: @night-hover;
        }
      }

      .highlight {
        a {
          background-color: @night-hover;
          color: @night-title;
        }
      }
    }
  }
}
</style>
