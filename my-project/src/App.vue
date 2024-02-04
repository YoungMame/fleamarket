<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    <router-link to="'/product/' + 1">Produit</router-link>
  </nav>
  <router-view/>
  <div class="container">
    <footer class="d-flex flex-wrap justify-content-between align-items-center py-3 my-4 border-top">
      <p class="col-md-4 mb-0 text-body-secondary">&copy; 2023 Company, Inc</p>

      <a href="/" class="col-md-4 d-flex align-items-center justify-content-center mb-3 mb-md-0 me-md-auto link-body-emphasis text-decoration-none">
        <svg class="bi me-2" width="40" height="32"><use xlink:href="#bootstrap"/></svg>
      </a>

      <ul class="nav col-md-4 justify-content-end">
        <li class="nav-item"><a href="#" class="nav-link px-2 text-body-secondary nav-a">Home</a></li>
        <li class="nav-item"><a href="#" class="nav-link px-2 text-body-secondary nav-a">Features</a></li>
        <li class="nav-item"><a href="#" class="nav-link px-2 text-body-secondary nav-a">Pricing</a></li>
        <li class="nav-item"><a href="#" class="nav-link px-2 text-body-secondary nav-a">FAQs</a></li>
        <li class="nav-item"><a href="#" class="nav-link px-2 text-body-secondary nav-a">About</a></li>
      </ul>
    </footer>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import { ref } from 'vue'
import productsData from './assets/products.json'
export default {
  setup() {
    const products = ref(productsData)

    return {
      products
    }

    console.log(productsData)
  }
}
</script>
