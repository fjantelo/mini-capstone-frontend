<script>
export default {
  data: function () {
    return {
      newProduct: {},
    };
  },
  created: function () {},
  methods: {},
};
</script>

<template>
  <div>
    <h1>New Product</h1>
    <label>Name</label>
    <input type="text" v-model="newProduct.name" />
    |
    <label>Price</label>
    <input type="text" v-model="newProduct.price" />
    |
    <label>Description</label>
    <input type="text" v-model="newProduct.description" />
    |
    <label>Supplier ID</label>
    <input type="text" v-model="newProduct.supplier_id" />
  </div>
  <p></p>
  <button v-on:click="saveProduct()">Save</button>
</template>

<style></style>
