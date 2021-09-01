<template>
  <button class="button" :class="variant">
    <slot />
  </button>
</template>

<style scoped>
.button {
  background-color: #333;
  border: 0;
  border-radius: 1rem;
  color: #fff;
  font-family: sans-serif;
  padding: 0.5rem 1rem;
}
.button:hover {
  background-color: #777;
}

.variant-a {
  background-color: hsl(217, 100%, 50%);
}
.variant-a:hover {
  background-color: hsl(217, 100%, 75%);
}

.variant-b {
  background-color: hsl(55, 100%, 50%);
  color: #000;
}
.variant-b:hover {
  background-color: hsl(55, 100%, 75%);
}
</style>

<script>
export default {
  name: 'Button',
  props: {
    variant: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      variant: this.variant,
    }
  }
}
</script>
