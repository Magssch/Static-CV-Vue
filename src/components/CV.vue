<template>
  <div class="cv">
    <h1>{{ name }}</h1>
    <h2>{{ title }}</h2>
    <CVArea name="Erfaring" :fields="jobbFields" icon="work" />
    <CVArea name="Utdanning" :fields="skoleFields" icon="school" />
    <CVArea name="Verv" :fields="vervFields" icon="group"  />
  </div>
</template>

<script>
import CVArea from "./CVArea";

export default {
  name: 'CV',

  props: {
    name: String,
    title: String,
      vervFields: [],
      jobbFields: [],
      skoleFields: []
  },

  components: {
      CVArea
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .cv {
    background-color: azure;
    padding: 4px;
    display: flex;
    flex-direction: column;
  }

  h1 {
    margin: 20px 0 0;
  }

  h2 {
    margin: 20px 0 0;
  }

  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
