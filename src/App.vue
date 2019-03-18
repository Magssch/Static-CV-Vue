<template>
  <div class="app">
    <img alt="Profile pic" src="./assets/pb.jpg" class="pb">
    <CV name="Magnus Schjølberg" title="Sjef - Generelt AS"
        :jobbFields="
          [
            'Sjef, Generelt AS',
            'Skribent, Dagens Narringsliv',
            'Sjefssjef, Sjefstad AS'
          ]
        "
        :vervFields="
          [
            'Ryddegutt, McDonalds',
            'Backer, Falafelboyz 0287'
          ]
        "
        :skoleFields="
          [
            'Datateknologi, NTNU',
            'Livsnyter, Livets Harde Skole'
          ]
        "

    />
  </div>
</template>

<script>
import CV from './components/CV.vue'

export default {
  name: 'app',
    data() {
      return {
          pbHover: false
      }
    },
  components: {
    CV
  }
}
</script>

<style>
  body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    background-color: lightblue;
  }

  .app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: lightblue;
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
  }

  .pb {
    border-radius: 200px;
    height: 270px;
    padding: 20px;
    transition: all .2s ease-in-out;
  }

  .pb:hover { transform: scale(1.1); }

</style>
