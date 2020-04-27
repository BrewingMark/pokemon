<template lang="html">
  <div>
    <li>{{card.name}}<img v-bind:src="card.imageUrlHiRes" alt="pokemon card"></li>
  </div>
</template>

<script>
export default {
  name: 'list-item',
  props: ['card'],
}
</script>

<style lang="css" scoped>
</style>
