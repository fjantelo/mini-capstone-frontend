<script>
import axios from "axios";

export default {
  data: function () {
    return {
      products: [],
    };
  },
  created: function () {
    this.getProducts();
  },
  methods: {
    getProducts: function () {
      axios.get("/products.json").then((response) => {
        this.products = response.data;
        console.log(response);
      });
    },
  },
};
</script>

<template>
  <h1>All Products</h1>
  <div v-for="product in products" v-bind:key="product.id">
    <router-link :to="`/products/${product.id}`">
      <h4>{{ product.name }}</h4>
    </router-link>
    <p>${{ product.price }}</p>
    <p>{{ product.description }}</p>
    <img :src="product.images[0].url" />
  </div>
</template>

<style></style>
