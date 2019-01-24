<template>
  <div id="app">
    <h1>Shopping Cart Example</h1>
    <hr>
    <h2>Products</h2>
    <ProductList/>
    <hr>
    <ShoppingCart/>
  </div>
</template>

<script>
import ProductList from './ProductList.vue'
import ShoppingCart from './ShoppingCart.vue'
export default {
  components: { ProductList, ShoppingCart }
}
</script>

<style scoped>
html, body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    color: #2c3e50;
  }
  
  ul {
    line-height: 1.5em;
    padding-left: 1.5em;
  }
  
  a {
    color: #7f8c8d;
    text-decoration: none;
  }
  
  a:hover {
    color: #4fc08d;
  }  
</style>
