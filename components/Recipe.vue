<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div class="thumbnail" :style="{backgroundImage: `url(${thumbnail})`}"></div>
      <h1>{{ title }}</h1>
      <p>{{ preview }}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: ['thumbnail', 'title', 'preview', 'id']
}
</script>

<style>
.recipe {
    box-sizing: border-box;
    width: 280px;
    border: 1px solid brown;
    height: 300px;
  }

  .thumbnail {
    background-size: cover;
    height: 300px;
  }
</style>
