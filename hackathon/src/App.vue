<template>
  <div>
    <nav class="navbar">
      <a href="#">Dashboard</a>
      <a href="#">Manager Category</a>
      <a class="active" href="#">Manager Product</a>
    </nav>
    <ProductTable />
  </div>
</template>

<script setup>
import ProductTable from './components/ProductTable.vue';

</script>

<style>
.navbar {
  background-color: black;
  padding: 1rem;
}
.navbar a {
  color: white;
  padding: 0.5rem 1rem;
  text-decoration: none;
}
.navbar a.active {
  background-color: grey;
}
</style>