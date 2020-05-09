<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
      <div class="button is-primary">Show Detail</div>
    </article>
  </nuxt-link>
</template>

<script>
  export default {
    props: ['id', 'thumbnail', 'title', 'previewText']
  }
</script>

<style lang="sass" scoped>
a
  text-decoration: none
  color: black

.recipes
  display: flex

.recipe
  border: 1px solid #ddd
  border-radius: 4px
  padding: 8px
  margin: 8px
</style>
