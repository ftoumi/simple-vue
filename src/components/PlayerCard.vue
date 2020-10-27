<template>
  <div class="border border-green-900 m-2 p-2 rounded bg-gray-300">
    <h3>{{ playerName }} ({{ player.number }})</h3>
    <p>{{ player.position }}</p>
  </div>
  
</template>

<script>
export default {
  name: "player-card",
  props: ['player'],
  computed: {
    playerName() {
      if(this.player.name.split('.').length > 1){
        return this.player.name.split('.')[1]
      }
      return this.player.name;
    }
  }
}
</script>

<style scoped>

</style>