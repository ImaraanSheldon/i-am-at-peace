<template>
  <div id="app">
    <FriendsComp />
    <ProductsComp />
  </div>
</template>

<script>
import FriendsComp from './components/FriendsComp.vue';
import ProductsComp from './components/ProductsComp.vue';

export default {
  name: 'App',
  components: {
    FriendsComp,
    ProductsComp
  }
};
</script>

<style>
/* Optional: Add custom styles for App component */
body, h2{
  background-color: #ccc7c7;
}
</style>
