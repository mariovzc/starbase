<template>
  <div>
    {{items}}
  </div>
</template>
<script>
export default {
  data () {
    return {
      type: this.$route.params.type,
      items: []
    }
  },
  watch: {
    '$route': 'fetchItems'
  },
  methods: {
    fetchItems () {
      this.items = []
      this.type = this.$route.params.type
      let initial_ids = [1, 13, 14]
      initial_ids.forEach(id => {
        console.log(id) 
        fetch(`https://swapi.co/api/${this.type}/${id}`,{
          method: 'GET'
        })
        .then(response => response.json())
        .then( json => this.items.push(json))
      })
    }
  },
  created() {
    this.fetchItems()
  }
}
</script>
