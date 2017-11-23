<template>
  <div class="col-md-4">
    <div class="character-card">
      <div class="card-block">
        <h4 class="card-title">{{item.name}}</h4>
        <div 
          v-for="(value, key, index) in item" 
          v-bind:key="index"
        >
          <div v-if="index < 5">
            <strong>{{key}}</strong>: {{value}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ['item']
}
</script>
<style scoped>
.character-card{
  border: 2px solid #4FC08D;
  border-radius: 4px;
  cursor: pointer;
  padding: 5px;
  padding-bottom: 10px;
}
</style>

