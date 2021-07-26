<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">Starting page</nuxt-link></li>
        <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style>
  header {
    width: 100%;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: burlywood;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    align-items: center;
  }

  li {
    margin: 0 10px;
  }
</style>
