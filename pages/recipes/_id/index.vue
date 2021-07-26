<template>
  <section class="single-recipe">
    <p>Route: {{ $route.params.id }} - typeof: {{ typeof ($route.params.id) }}</p>
    <h3>{{ recipe.title }}</h3>
    <p>index dentro recipes</p>
  </section>
</template>

<style>
 .single-recipe {
   border: 1px solid rosybrown;
 }
</style>

<script>
export default {
    asyncData (context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1", // necessariamente stringa e NON numero, perché si deve confrontare con il contex id param (stringa)
              title: 'Pizza',
              preview: 'La pizza è buonissima',
              thumbnail: 'http://www.delonghi.com/Global/recipes/multifry/pizza_fresca.jpg'
            },
            {
              id: "2",
              title: 'Torta',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: "3",
              title: 'Torta id 3',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: "4",
              title: 'Torta id 4',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            },
            {
              id: "5",
              title: 'Torta id 5',
              preview: 'La torta è ancora più buona della pizza',
              thumbnail: 'https://blog.giallozafferano.it/ricettepanedolci/wp-content/uploads/2017/10/torta-alla-nutella-e-crema-pasticcera.jpg'
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500);
    })
  }
}
</script>

