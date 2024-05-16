<script setup>
let friends = ["Asma", "Sakib", "joy", "rakib"];

const products = [
  {
    name: "DataVista T Shirt",
    description: "Lorem ipsum dolor, sit amet.",
    price: 25.99,
    category: "Apparel",
  },
  {
    name: "Exploretech Hoddie",
    description: "Lorem ipsum dolor, sit amet.",
    price: 39.99,
    category: "Apparel",
  },
  {
    name: "Alpine Bottle",
    description: "Lorem ipsum dolor, sit amet.",
    price: 18.99,
    category: "Accessories",
  },
];
</script>

<template>
    <!-- <li v-for="(friend, index) in friends" :key="index">{{ index }} {{friend}}</li> -->

    <div >
      <table>
        <tr>
          <th>SL No.</th>
          <th>Name :</th>
          <th>Description :</th>
          <th>Price :</th>
          <th>Category :</th>
        </tr>
        <tr v-for="(product, index) in products" :key="index">
          <td>{{ index }}</td>
          <td>{{ product.name }}</td>
          <td>{{ product.description }}</td>
          <td>{{ product.price }}</td>
          <td>{{ product.category }}</td>
        </tr>
      </table>
    </div>
</template>

<style scoped>
table,th,td{
  border: 1px solid #000;
}
</style>
