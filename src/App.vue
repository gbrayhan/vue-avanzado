<template lang="pug">
  #app
    img(src= "./assets/logo.png")
    h1 {{ msg }}
    p {{ 'Hola ' + 'Mundo'}}
    p {{ person.name }}
    p {{ person.name.toUpperCase() }}
    p {{ JSON.stringify(person) }}
    p {{ condicion ? 'Es Verdadero' : 'Es Falso' }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hola Mundo vuejs',
      person: {
        name: 'Alex'
      },
      condicion: false
    }
  }
}
</script>

<style lang="scss">
  @import "./scss/main.scss";
</style>
