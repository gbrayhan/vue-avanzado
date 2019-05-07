<template lang="pug">
  #app
    input(v-model="name")
    input(v-model="lastName")

    p {{ fullname }}
</template>
<script>
export default {
  name: 'app',
  data () {
    return {
      name: '',
      lastName: ''
    }
  },
  computed: {
    fullname () {
      // return this.name + '' + this.lastName
      return `${this.name} ${this.lastName}`
    }
  }
}
</script>
<style lang="scss">
  @import "./scss/main.scss";
</style>
