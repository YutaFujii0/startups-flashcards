<template>
  <div class="container">
    <div class="buttion is-primary">New quiz</div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        question: '',
        choices: []
      }
    },
    async fetch() {

    },
    method: {
      getStartupProfiles() {
        axios.get()
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
