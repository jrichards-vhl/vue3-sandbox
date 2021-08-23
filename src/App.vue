<script>
import Parent from './components/parent/Parent.vue';
import Child from './components/child/Child.vue';

export default {
  name: 'App',
  components: {
    Parent,
    Child,
  }
}
</script>

<template>
  <div class="root">
    <Parent>
      <Child></Child>
    </Parent>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/*
.some_non-scoped_class {
  background-color: #faa;
  color: #fff;
  font-family: monospace;
  font-size: 1.2rem;
}
*/

.c-panel {
  display: block;
  background-color: #00f;
  border-radius: 0.5rem;
  padding: 2rem;
}
.c-panel--sunset {
  background-color: #f90;
}

</style>
