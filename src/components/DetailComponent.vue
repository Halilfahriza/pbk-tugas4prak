<template>
    <div class="detail">
      <h2>Detail View</h2>
      <p><strong>Name:</strong> {{ item.name }}</p>
      <p><strong>Description:</strong> {{ item.description }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      item: Object
    }
  };
  </script>
  
  <style scoped>
  .detail {
    border: 1px solid #000;
    padding: 20px;
    margin-top: 20px;
    background-color: #b41616;
    border-radius: 10px;
  }
  </style>
  