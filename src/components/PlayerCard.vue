<template>
  <h3>{{ player.name }} ({{ player.number }})</h3>
  <p>{{ player.position }}</p>
</template>

<script>
export default {
  name: "player-card",
  props: ['player']
}
</script>

<style>

</style>