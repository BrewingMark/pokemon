<template lang="html">
  <div>
    <ul>
      <list-item v-for="(card, index) in cards" :card="card" :key="index"></list-item>
    </ul>
  </div>
</template>

<script>

import ListItem from './ListItem.vue'

export default {
  name: 'cards-list',
  props: ['cards'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style lang="css" scoped>
</style>
