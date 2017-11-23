<template>
  <div id="app">
    <h3>{{ title }}</h3>
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
<style lang="sass" scoped>

</style>
