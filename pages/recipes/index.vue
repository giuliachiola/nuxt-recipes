<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :preview="recipe.preview"
      :id="recipe.id"/>
  </section>
</template>

<style>
  .recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
  }
</style>

<script>
import Recipe from '@/components/Recipe'
export default {
  components: {
    Recipe
  },

  asyncData () {
    // fake async request --> il template si re-render solo quando la promise è risolta
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: 1,
              title: 'Pizza',
              preview: 'La pizza è buonissima',
              thumbnail: 'http://www.delonghi.com/Global/recipes/multifry/pizza_fresca.jpg'
            },
            {
              id: 2,
              title: 'Torta',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: 3,
              title: 'Torta id 3',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: 4,
              title: 'Torta id 4',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: 5,
              title: 'Torta id 5',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            }
          ]
        })
      }, 1500);
    })
  }
}
</script>
