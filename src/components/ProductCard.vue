<script setup>
const componentProp = defineProps(["productList"]);
</script>
<template>
  <div v-for="product in componentProp.productList">
    <div class="main-container" :id="product.id">
      <h2>{{ product.name }}</h2>
      <h4>Precio: {{ product.price }}</h4>
      <img
        v-if="product?.image"
        class="product-image"
        :src="`/images/${product.image}`"
      />
      <p v-else>Imagen del producto no disponible</p>
      <p>{{ product.description }}</p>
    </div>
  </div>
</template>

<style lang="css" scoped>
.main-container {
  font-size: large;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: rgb(189, 90, 90);
  border: 10px;
  border-radius: 10px;
  padding: 3%;
  margin: 1%;
  color: #fff;
}
.product-image {
  width: auto;
  height: auto;
  max-width: 200px;
  max-height: 200px;
  border-radius: 10%;
}
</style>
