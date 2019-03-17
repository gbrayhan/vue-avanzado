<template>
  <div id="app">
    <img src="./assets/logo.png" alt="Vuejs"/>
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hola Mundo vuejs'
    }
  }
}
</script>

<style lang="scss">
</style>
