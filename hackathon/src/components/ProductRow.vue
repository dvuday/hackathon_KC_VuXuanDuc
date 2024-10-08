<template>
  <tr>
    <td>{{ index }}</td>
    <td><img :src="product.image" alt="" class="product-image" /></td>
    <td>{{ product.name }}</td>
    <td>{{ product.price }}</td>
    <td>{{ product.quantity }}</td>
    <td>
      <button class="edit-button">Edit</button>
      <button class="delete-button">Delete</button>
    </td>
  </tr>
</template>

<script>
export default {
  props: {
    product: Object,
    index: Number
  }
}
</script>

<style>
.product-image {
  width: 50px;
  height: 50px;
}
.edit-button {
  background-color: orange;
  color: white;
  padding: 0.5rem 1rem;
  border: none;
}
.delete-button {
  background-color: red;
  color: white;
  padding: 0.5rem 1rem;
  border: none;
}
</style>