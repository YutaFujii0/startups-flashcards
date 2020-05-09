<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :id="recipe.id"
      :title="recipe.title"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },
  data: {
    pageTitle: "this is recipess page"
  },
  asyncData() {
    // return axios.get()
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Margelita",
              previewText: "Awesome Pizza"
            },
            {
              id: "2",
              title: "Sea food salad",
              previewText: "Fresh and tasty"
            }
          ]
        })
      }, 1500)
    })
  }
}
</script>

<style lang="sass" scoped>
.recipes
  display: flex

.recipe
  border: 1px solid #ddd
  border-radius: 4px
  padding: 8px
  margin: 8px
</style>
