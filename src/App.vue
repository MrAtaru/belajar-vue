<template>
  <div>
    <h1>Aplikasi Vue.js saya</h1>
    <my-component nama="Athhar" umur="18"></my-component>
  </div>
</template>

<script>
import MyComponent from './MyComponent.vue';

export default {
  components: {
    MyComponent
  }
}
</script>