<template>
    <div id="app">
        <HelloWorld/>
    </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'

  export default {
    name: 'App',
    data() {
      return {}
    },
    components: {
      HelloWorld
    }
  }
</script>

<style lang="scss">
    @import "assets/css/reset.css";
</style>
