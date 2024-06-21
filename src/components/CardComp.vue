<template>
    <div class="card">
      <div class="card-header">
        <slot name="cardHeader"></slot>
      </div>
      <div class="card-body">
        <slot name="cardBody"></slot>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CardComp'
  };
  </script>
  
  <style>
  .card {
    border: 1px solid #000;
    border-radius: 4px;
    margin-bottom: 15px;
  }
  
  .card-header {
    background-color: #000;
    padding: 10px;
  }
  
  .card-body {
    padding: 15px;
  }
  </style>