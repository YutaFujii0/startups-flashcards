<template>
  <div class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <p>{{ recipe.previewText }}</p>
  </div>
</template>

<script>
  export default {
    asyncData(context) {
      // return axios.get()
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            recipe: [
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
            ].find(el => el.id === context.params.id)
          })
        }, 1500)
      })
    }
  }
</script>

<style lang="scss" scoped>

</style>
