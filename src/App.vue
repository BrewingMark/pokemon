<template lang="html">
  <div>
    <h1>browse cards</h1>
    <cards-list :cards="cards"></cards-list>
  </div>
</template>

<script>

import CardsList from './components/CardsList.vue';

export default {
  name: 'app',
  data() {
    return {
      pokedex: [],
      cards: []
    }
  },
  mounted(){
    fetch('https://api.pokemontcg.io/v1/cards')
    .then(result => result.json())
    .then(cards => this.cards = cards)
  },
  components: {
    "cards-list": CardsList,
  }
}
</script>

<style lang="css" scoped>
</style>
