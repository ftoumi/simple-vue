<template>
  <h1>Liste des joueurs {{ playersData.name }} </h1>

  <selection-box 
    :selection="selection"
  >
  </selection-box>

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
import SelectionBox from './SelectionBox.vue'

export default {
  name: "player-List",
  components: {
    PlayerCard,
    SelectionBox
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