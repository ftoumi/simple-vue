<template>
  <h1>Liste des joueurs {{ playersData.name }} </h1>

  <div>Sélection XX joueurs</div>

  <player-card
    v-for="(player, index) in playersData.players"
    :key="index"
    :player="player"
    >
  </player-card>

</template>

<script>

import playersData from '../assets/data/players.json'
import PlayerCard from './PlayerCard.vue'

export default {
  name: "player-List",
  components: {
    PlayerCard
  },
  data() {
    return {
      playersData : playersData
    }
  }
}
</script>

<style>

</style>