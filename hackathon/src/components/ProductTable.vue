<template>
  <div class="product-table">
    <h2>Manager Product</h2>
    <button class="add-button">Add New Product</button>
    <table>
      <thead>
        <tr>
          <th>STT</th>
          <th>Image</th>
          <th>Name</th>
          <th>Price</th>
          <th>Quantity</th>
          <th>Option</th>
        </tr>
      </thead>
      <tbody>
        <ProductRow v-for="(product, index) in products" :key="index" :product="product" :index="index + 1" />
      </tbody>
    </table>
  </div>
</template>

<script>
import ProductRow from './ProductRow.vue';

export default {
  components: {
    ProductRow
  },
  data() {
    return {
      products: [
        { name: 'Orange', image: 'https://o.rada.vn/data/image/2021/03/26/Ta-qua-cam-700.jpg', price: '30,000 đ', quantity: 100 },
        { name: 'Apple', image: 'https://anhdephd.vn/wp-content/uploads/2022/05/hinh-anh-qua-tao.jpg', price: '20,000 đ', quantity: 50 },
        { name: 'Banana', image: 'https://i.khoahoc.tv/photos/image/2018/08/10/qua-chuoi.jpg', price: '25,000 đ', quantity: 200 },
        { name: 'Grape', image: 'https://pantado.edu.vn/storage/media/qua-nho-trong-tieng-anh-la-gi%20(1)_1640568040.jpg', price: '60,000 đ', quantity: 80 },
        { name: 'Watermelon', image: 'https://th.bing.com/th/id/R.0055b58f7ea7531ff1d8318421f8e169?rik=urKFneEZXfKX8Q&riu=http%3a%2f%2fatvstphagiang.org.vn%2fphoto%2fnam-2019%2fthang-6%2f2-2.jpg&ehk=O%2bXy9516gQQ4a5MSseloY0n2ofPr%2b8ANjZa5vFbhd2w%3d&risl=&pid=ImgRaw&r=0', price: '30,000 đ', quantity: 30 }
      ]
    };
  }
}
</script>

<style>
.product-table {
  padding: 1rem;
}
table {
  width: 100%;
  border-collapse: collapse;
}
th, td {
  border: 1px solid #ddd;
  padding: 8px;
}
.add-button {
  background-color: blue;
  color: white;
  padding: 0.5rem 1rem;
  border: none;
  margin-bottom: 1rem;
}
</style>