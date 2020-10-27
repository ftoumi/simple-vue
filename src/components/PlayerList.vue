<template>
  <h1>Liste des joueurs {{ playersData.name }} </h1>

  <div>Ma sélection : {{ selection.length }} joueur</div>

  <player-card
    v-for="(player, index) in playersData.players"
    :key="index"
    :player="player"
    @add-player="addPlayerToSelection"
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
      playersData : playersData,
      selection: []
    }
  },
  methods: {
    addPlayerToSelection(player) {
      this.selection.push(player)
    }
  }
}
</script>

<style>

</style>