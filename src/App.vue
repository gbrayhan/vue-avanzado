<template lang="pug">
  #app
    p(v-show="showValue") {{ value }}
    p(v-if="showValue") {{ value }}
    p(v-else-if="condicion") {{ "recurso alterno" }}
    p(v-else) {{ 'recurso no disponible' }}
    ul
      li(v-for="item in items") {{ item * 2 }}
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
      condicion: true,
      showValue: false,
      value: 'Elemento a Mostrar',
      items: [1, 2, 3, 4, 5, 6, 7, 5, 4, 3, 2, 3]
    }
  }
}
</script>

<style lang="scss">
  @import "./scss/main.scss";
</style>
