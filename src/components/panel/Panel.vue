<script>
  export default {
    name: 'Panel',
    props: {
      theme: {
        type: String,
        required: false
      }
    }
  }
</script>

<template>
  <!-- See App.vue where ".c-panel" is defined. -->
  <div class="c-panel" :class="theme === 'sunset' ? 'c-panel--sunset' : ''">
    <slot></slot>
  </div>
</template>

