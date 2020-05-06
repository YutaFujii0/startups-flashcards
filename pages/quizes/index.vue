<template>
  <div class="container">
    <div class="buttion is-primary">Start Quiz</div>
    <div>{{ question }}</div>
    <div v-for="choice in choices">{{ choice.name }}</div>
  </div>
</template>

<script>
  import axios from 'axios'
  import cheerio from 'cheerio';

  export default {
    data() {
      return {
        question: '',
        choices: [
          { name: "Choice 1" },
          { name: "Choice 2" },
          { name: "Choice 3" },
          { name: "Choice 4" }
        ]
      }
    },
    created() {
      this.getStartupProfiles()
    },
    methods: {
      async getStartupProfiles() {
        const html = await axios
          .get('http://hrmc.lvh.me:3000/sdb/')
          .catch((err) => {
            console.log("error caused:", err)
          })
        const $ = await cheerio.load(html.data)
        this.question = $('.p-btn__modal a').text()
      }
    }
  }
</script>

<style scoped lang="sass">
</style>
