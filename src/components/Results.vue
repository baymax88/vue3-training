<template>
  <p>Reaction Time - {{ score }}</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Ninja Figers'
    } else if (this.score < 400) {
      this.rank = 'Rapid reflexes'
    } else {
      this.rank = 'Snail Pace ...'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>