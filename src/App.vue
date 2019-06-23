<template>
  <div id="app">
    <section class="section">
      <nav class="nav has-shadow">
        <div class="container">
          <input type="text" class="input is-large" placeholder="buscar canciones" v-model="searchQuery">
          <a href="" class="button is-info is-large" @click.prevent="search">Buscar</a>
          <a href="" class="button is-danger is-large">&times;</a>
        </div>
      </nav>

      <div class="container results">
        <div class="colums">
          <div class="column items" v-for="(track, index ) in tracks" :key="index">
            {{track.name}} - {{track.artist}}
          </div>
          <p class="help is-success">Resultados encontrados: {{searchMesssage}}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
const tracks = [
  { name: 'muchacha', artist: 'Luis albeto' },
  { name: 'vivir la vida', artist: 'Marck antony' },
  { name: 'Platzi', artist: 'Nacho' }
]

export default {
  name: 'app',
  data () {
    return {
      searchQuery: '',
      tracks: []
    }
  },
  methods: {
    search () {
      this.tracks = tracks
    }
  },
  computed: {
    searchMesssage () {
      return this.tracks.length
    }
  }
}
</script>

<style lang="scss">
@import 'scss/main.scss';

#app {
  .custom {
    margin-top: 20px;
  }

  .items {
    padding: 5px;
  }
}
</style>
