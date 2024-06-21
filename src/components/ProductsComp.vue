<template>
    <div>
      <h2 class="text-center p-3">Products List</h2>
      <div v-if="products.length === 0">Loading spinner...</div>
      <div v-else>
        <div v-for="product in products" :key="product.id" class="card">
          <h4 class="card-header text-center fw-bold">{{ product.name }}</h4>
          <div class="card-body d-flex align-items-center flex-column">
            <img :src="product.profile" alt="ProductImage">
            <p>Description: {{ product.description }}</p>
            <p>Price: {{ product.price }}</p>
            <p>Status: {{ product.status }}</p>
            <!-- Add more details as needed -->
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductsComp',
    data() {
      return {
        products: [
          { id: 1, name: 'Product 1', description: 'Description 1', price: '$100', profile:'Portrait_Placeholder.png', status: 'Available' },
          { id: 2, name: 'Product 2', description: 'Description 2', price: '$50', profile:'Portrait_Placeholder.png', status: 'Out of Stock' }
          // Add more products as needed
        ]
      };
    }
  };
  </script>
  
  <style>
  /* Optional: Add custom styles for Products component */
  .card {
    margin: auto;
    width: 50vw;
    margin-bottom: 20px;
  }
  </style>