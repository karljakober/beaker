<template>
  <div>
    <div class="section">
      <h1>Buttons</h1>
      <p>Our button component is super flexible. It can act as type <code>button</code>, <code>a</code> tag or <code>router-link</code>. Please note that you may need to use 'ButtonInput' rather than 'Button' to avoid issues.</p>
    </div>
    <div class="section">
      <h2>Standard Buttons</h2>
      <p>Used throughout website Dashboard and Streamlabs OBS.</p>
      <div class="section">
        <h3>Active</h3>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :variation=&quot;'default'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'action'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'warning'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'default'&quot;
    :title=&quot;'with icon'&quot;
    :icon=&quot;'settings'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
          </div>
        </Accordion>
        <div class="button-container button-container--left">
          <Button
            :variation="'default'"
            :title="'Default'">
          </Button>

          <Button
            :variation="'action'"
            :title="'Action'">
          </Button>

          <Button
            :variation="'warning'"
            :title="'Warning'">
          </Button>

          <Button
            :variation="'default'"
            :title="'with icon'"
            :icon="'settings'">
          </Button>
        </div>
      </div>
      <div class="section">
        <h3>Disabled</h3>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'disabled'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'action'&quot;
    :state=&quot;'disabled'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'warning'&quot;
    :state=&quot;'disabled'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'disabled'&quot;
    :title=&quot;'with icon'&quot;
    :icon=&quot;'edit'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
          </div>
        </Accordion>
        <div class="button-container button-container--left">
          <Button
            :variation="'default'"
            :state="'disabled'"
            :title="'Default'">
          </Button>

          <Button
            :variation="'action'"
            :state="'disabled'"
            :title="'Action'">
          </Button>

          <Button
            :variation="'warning'"
            :state="'disabled'"
            :title="'Warning'">
          </Button>

          <Button
            :variation="'default'"
            :state="'disabled'"
            :title="'with icon'"
            :icon="'edit'">
          </Button>
        </div>
      </div>
      <div class="section">
        <h3>Focus</h3>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'focused'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'action'&quot;
    :state=&quot;'focused'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'warning'&quot;
    :state=&quot;'focused'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'focused'&quot;
    :title=&quot;'with icon'&quot;
    :icon=&quot;'edit'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
          </div>
        </Accordion>
        <div class="button-container button-container--left">
          <Button
            :variation="'default'"
            :state="'focused'"
            :title="'Default'">
          </Button>

          <Button
            :variation="'action'"
            :state="'focused'"
            :title="'Action'">
          </Button>

          <Button
            :variation="'warning'"
            :state="'focused'"
            :title="'Warning'">
          </Button>

          <Button
            :variation="'default'"
            :state="'focused'"
            :title="'with icon'"
            :icon="'edit'">
          </Button>
        </div>
      </div>
      <div class="section">
        <h3>Loading</h3>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'loading'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'action'&quot;
    :state=&quot;'loading'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'warning'&quot;
    :state=&quot;'loading'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :variation=&quot;'default'&quot;
    :state=&quot;'loading'&quot;
    :title=&quot;'with icon'&quot;
    :icon=&quot;'edit'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
          </div>
        </Accordion>
        <div class="button-container button-container--left">
          <Button
            :variation="'default'"
            :state="'loading'"
            :title="'Default'">
          </Button>

          <Button
            :variation="'action'"
            :state="'loading'"
            :title="'Action'">
            Action
          </Button>

          <Button
            :variation="'warning'"
            :state="'loading'"
            :title="'Warning'">
            Warning
          </Button>

          <Button
            :variation="'default'"
            :state="'loading'"
            :title="'with icon'"
            :icon="'recent-events'">
          </Button>
        </div>
        <p>Click <a @click="isLoadingExample = !isLoadingExample">here</a> to test.</p>
        <Button
          :class="{ 'is-loading': isLoadingExample }"
          :type="'button'"
          :variation="'default'"
          :title="'with icon'"
          :icon="'pop-out-1'">
        </Button>
      </div>
    </div>
    <div class="section">
      <h2>Medium Buttons</h2>
      <p>Medium is the size used on the App Store and the Tip page. It is slightly larger than our standard button.</p>
      <Accordion
        :openedTitle="'Hide Code'"
        :closedTitle="'Show Code'">
        <div slot="content">
          <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'medium'&quot;
    :variation=&quot;'default'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'medium'&quot;
    :variation=&quot;'action'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'medium'&quot;
    :variation=&quot;'warning'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'medium'&quot;
    :variation=&quot;'default'&quot;
    :title=&quot;'With Icon'&quot;
    :icon=&quot;'image'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
        </div>
      </Accordion>
      <div class="button-container button-container--left">
        <Button
          :type="'button'"
          :size="'medium'"
          :variation="'default'"
          :title="'Default'">
        </Button>

        <Button
          :type="'button'"
          :size="'medium'"
          :variation="'action'"
          :title="'Action'">
        </Button>

        <Button
          :type="'button'"
          :size="'medium'"
          :variation="'warning'"
          :title="'Warning'">
        </Button>

        <Button
          :type="'button'"
          :size="'medium'"
          :variation="'default'"
          :title="'With Icon'"
          :icon="'image'">
        </Button>
      </div>
    </div>
    <div class="section">
      <h2>Large Buttons</h2>
      <p>Used on website marketing pages and for the Donate button on the tip page.</p>
      <Accordion
        :openedTitle="'Hide Code'"
        :closedTitle="'Show Code'">
        <div slot="content">
          <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'large'&quot;
    :variation=&quot;'default'&quot;
    :title=&quot;'Default'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'large'&quot;
    :variation=&quot;'action'&quot;
    :title=&quot;'Action'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'large'&quot;
    :variation=&quot;'warning'&quot;
    :title=&quot;'Warning'&quot;&gt;
  &lt;/Button&gt;

  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'large'&quot;
    :variation=&quot;'default'&quot;
    :title=&quot;'With Icon'&quot;
    :icon=&quot;'image'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
        </div>
      </Accordion>
      <div class="button-container button-container--left">
        <Button
          :type="'button'"
          :size="'large'"
          :variation="'default'"
          :title="'Default'">
        </Button>

        <Button
          :type="'button'"
          :size="'large'"
          :variation="'action'"
          :title="'Action'">
        </Button>

        <Button
          :type="'button'"
          :size="'large'"
          :variation="'warning'"
          :title="'Warning'">
        </Button>

        <Button
          :type="'button'"
          :size="'large'"
          :variation="'default'"
          :title="'With Icon'"
          :icon="'image'">
        </Button>
      </div>
    </div>
    <div class="section">
      <h2>Full-Width Buttons</h2>
      <div class="section">
        <h3>Default</h3>
        <p>Used within cards and panels in the Dashboard.</p>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;Button
  :size=&quot;'full-width'&quot;
  :variation=&quot;'default'&quot;
  :title=&quot;'Start Giveaway'&quot;&gt;
&lt;/Button&gt;</code></pre>
          </div>
        </Accordion>
        <Button
          :size="'full-width'"
          :variation="'default'"
          :title="'Start Giveaway'">
        </Button>
      </div>
      <div class="section">
        <h3>Subscribe</h3>
        <p>Used on the App Platform for Subscribing to Apps.</p>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;Button
  :variation=&quot;'subscribe'&quot;
  :title=&quot;'Subscribe'&quot;
  :price=&quot;'$4.99'&quot;&gt;
&lt;/Button&gt;</code></pre>
          </div>
        </Accordion>
        <Button
          :variation="'subscribe'"
          :title="'Subscribe'"
          :price="'$4.99'">
        </Button>
      </div>
      <div class="section">
        <h3>Download</h3>
        <p>Used for Download Streamlabs OBS buttons.</p>
        <Accordion
          :openedTitle="'Hide Code'"
          :closedTitle="'Show Code'">
          <div slot="content">
            <pre>
<code>&lt;Button
  :variation=&quot;'slobs-download'&quot;
  :title=&quot;'Download Streamlabs OBS'&quot;
  :description=&quot;'Windows 7+ 245.8MB'&quot;&gt;
&lt;/Button&gt;</code></pre>
          </div>
        </Accordion>
        <Button
          :variation="'slobs-download'"
          :title="'Download Streamlabs OBS'"
          :description="'Windows 7+ 245.8MB'">
        </Button>
      </div>
    </div>
    <div class="section">
      <h2>Square Buttons</h2>
      <p>Used for add and subtract number inputs as well as login buttons.</p>
      <Accordion
        :openedTitle="'Hide Code'"
        :closedTitle="'Show Code'">
        <div slot="content">
          <pre>
<code>&lt;div class=&quot;button-container button-container--left&quot;&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'square'&quot;
    :variation=&quot;'default'&quot;
    :icon=&quot;'add'&quot;&gt;
  &lt;/Button&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :size=&quot;'square'&quot;
    :variation=&quot;'default'&quot;
    :icon=&quot;'subtract'&quot;&gt;
  &lt;/Button&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :variation=&quot;'facebook'&quot;
    :size=&quot;'square'&quot;
    :icon=&quot;'facebook'&quot;&gt;
  &lt;/Button&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :variation=&quot;'periscope'&quot;
    :size=&quot;'square'&quot;
    :icon=&quot;'periscope'&quot;&gt;
  &lt;/Button&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :variation=&quot;'mixer'&quot;
    :size=&quot;'square'&quot;
    :icon=&quot;'mixer'&quot;&gt;
  &lt;/Button&gt;
  &lt;Button
    :type=&quot;'button'&quot;
    :variation=&quot;'picarto'&quot;
    :size=&quot;'square'&quot;
    ::icon=&quot;'picarto'&quot;&gt;
  &lt;/Button&gt;
&lt;/div&gt;</code></pre>
        </div>
      </Accordion>
      <div class="button-container button-container--left">
        <Button
          :type="'button'"
          :size="'square'"
          :variation="'default'"
          :icon="'add'">
        </Button>
        <Button
          :type="'button'"
          :size="'square'"
          :variation="'default'"
          :icon="'subtract'">
        </Button>
        <Button
          :type="'button'"
          :variation="'facebook'"
          :size="'square'"
          :icon="'facebook'">
        </Button>
        <Button
          :type="'button'"
          :variation="'periscope'"
          :size="'square'"
          :icon="'periscope'">
        </Button>
        <Button
          :type="'button'"
          :variation="'mixer'"
          :size="'square'"
          :icon="'mixer'">
        </Button>
        <Button
          :type="'button'"
          :variation="'picarto'"
          :size="'square'"
          :icon="'picarto'">
        </Button>
      </div>
    </div>
    <div class="section">
      <h2>Navigation Buttons</h2>
      <p>Used to bring you between different page states.</p>
      <Accordion
        :openedTitle="'Hide Code'"
        :closedTitle="'Show Code'">
        <div slot="content">
          <pre>
<code>&lt;Button
  :variation=&quot;'navigation'&quot;
  :icon=&quot;'back'&quot;
  :title=&quot;'Back to Listings'&quot;&gt;
&lt;/Button&gt;</code></pre>
        </div>
      </Accordion>
      <Button
        :variation="'navigation'"
        :icon="'back'"
        :title="'Back to Listings'">
      </Button>
    </div>
    <table class="docs-table">
        <thead>
          <tr>
            <th>Prop</th>
            <th>Type</th>
            <th>Default</th>
            <th>Description</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>icon</td>
            <td>String</td>
            <td>null</td>
            <td>Use the endings of our custom icons. For example 'icon-settings' would be 'settings'. See icons page of the design system for a full list.</td>
          </tr>
          <tr>
            <td>title</td>
            <td>String</td>
            <td>null</td>
            <td>Main button text.</td>
          </tr>
          <tr>
            <td>price</td>
            <td>String</td>
            <td>null</td>
            <td>Used for subscribe buttons in the App Store.</td>
          </tr>
          <tr>
            <td>description</td>
            <td>String</td>
            <td>null</td>
            <td>Used for Streamlabs OBS download buttons to describe the version, size and compatibility.</td>
          </tr>
          <tr>
            <td>href</td>
            <td>String</td>
            <td>null</td>
            <td>Used if the the <code>type</code> is an <code>a</code> element (links).</td>
          </tr>
          <tr>
            <td>size</td>
            <td>String</td>
            <td>standard</td>
            <td>Size of the button. Options are <code>standard</code>, <code>medium</code>, <code>large</code>, <code>square</code>, and <code>full-width</code></td>
          </tr>
          <tr>
            <td>state</td>
            <td>String</td>
            <td>null</td>
            <td>State of the button. Options are <code>hover</code>, <code>focus</code>, <code>loading</code> and <code>disabled</code>.</td>
          </tr>
          <tr>
            <td>submit</td>
            <td>String</td>
            <td>null</td>
            <td>Set the button type to submit.</td>
          </tr>
          <tr>
            <td>to</td>
            <td>String</td>
            <td>null</td>
            <td>Used if the the <code>type</code> is a <code>router-link</code>. Define the path.</td>
          </tr>
          <tr>
            <td>type</td>
            <td>String</td>
            <td>button</td>
            <td>What type of element the component is. Options are <code>button</code>, <code>a</code>, <code>router-link</code></td>
          </tr>
          <tr>
            <td>variation</td>
            <td>String</td>
            <td>default</td>
            <td>The variation style of a button. Primary options are <code>default</code>, <code>action</code> and  <code>warning</code>. Other options are <code>subscribe</code>, <code>download</code> and <code>navigation</code>. Platform options are <code>facebook</code>, <code>mixer</code>, <code>twitch</code>, <code>yt</code>, <code>periscope</code> and <code>picarto</code>.</td>
          </tr>
        </tbody>
      </table>
  </div>
</template>


<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Accordion from "./../components/Accordion.vue";
import Button from "./../components/Button.vue";

@Component({
  components: {
    Accordion,
    Button
  }
})
export default class Forms extends Vue {
  isLoading = true;
  isLoadingExample = false;
}
</script>
