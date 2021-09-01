<script>
import Panel from '../panel/Panel.vue';
import Button from '../button/Button.vue';
export default {
  name: 'Parent',
  components: {
    Button,
    Panel
  },
}
</script>

<template>
  <div>
    <Button variant="variant-a">Hello world!</Button>
  </div>
  <div :class="$style.main">
    <Panel theme="sunset">
      <p :class="$style.copy">
        This is a parent component.
      </p>
    </Panel>
    <slot></slot>
  </div>
</template>

<style module>
.main {
  background-color: #000;
  padding: 1rem;
}

.copy {
  color: #fff;
  font-family: sans-serif;
  font-size: 1.5rem;
  text-align: left;
}

.c-panel {
  background-color: #f00;
}
</style>

