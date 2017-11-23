<template>
  <div id="app">
    <h3>{{ title }}</h3>
    <h4>
      <router-link class="link" to="/data/people">Meet the characters</router-link> | 
      <router-link class="link" to="/data/planets">Expore the Planets</router-link>|
      <router-link class="link" to="/data/vehicles">look the vehicles</router-link>
    </h4>
    <router-view></router-view>
  </div>
</template>
<script>
import Character from './components/Character.vue'

export default {
  name: 'app',
  data() {
    return {
      title: 'Generate your team',
      initial_ids: [1,13,14]
    }
  },
  components: {
    Character
  }
}
</script>
<style  scoped>
.link, .link:hover, .link:visited, .link:active {
  color: #4FC08D !important;
}
</style>
