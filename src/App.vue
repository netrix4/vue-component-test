<script setup>
import { ref } from "vue";
import BlogPost from "./components/BlogPost.vue";
import TaskItem from "./components/TaskItem.vue";
import ProductCard from "./components/ProductCard.vue";

const postList = ref([
  { id: 1, title: "Mucho calor en Enseyork", content: "Contenido1" },
  { id: 2, title: "titulo dosss" },
  { id: 3, title: "titulo tres", content: "contenido de tarjeta tres" },
  { id: 4 },
]);

const taskList = ref([
  {
    title: "Estudiar Vue",
    content: "debo estudiar vue",
    style: "background-color: #000;",
  },
  {
    title: "Hacer ejercicios de componentes",
    content: "Agarrar practica con componentes",
    style: "background-color: #fac300;",
  },
  {
    title: "Practicar props",
    content: "mas practica para props",
    style: "background-color: #000bab;",
  },
  {
    title: "Crear proyecto personal",
    content: "Es agarrar practica con u proyecto personal",
  },
]);

const productList = ref([
  {
    id: 1,
    name: "Latop gamer",
    price: 1299.99,
    image: "Laptop.png",
    description: "Laptop de alto rendimiento para gaming",
  },
  {
    id: 2,
    name: "Mac Mini (M2)",
    price: 1399.01,
    description: "Computadora de escritorio silenciosa con MacOS",
  },
  {
    id: 3,
    name: "Mouse Vertical",
    price: 99.99,
    image: "VerticalMouse.jpg",
    description: "Mouse ergónomico para computadora",
  },
]);
</script>
<template>
  <div class="card">
    <!-- <BlogPost :id="1" title="Mucho calor en ensenada" />
    <BlogPost :id="2" title="Mucho calor en ensenada" content="Esto es un contenido tambien" />
    <BlogPost :id="3" content="Esto es un contenido tambien" />
    <BlogPost :id="4" textColor="text-orange-500" />
    <BlogPost :id="5" colorFondo="#000" /> -->
    <!-- <BlogPost
      v-for="post in postList"
      :id="`${post.id}`"
      :title="`${post.title}`"
      :content="`${post.content}`"
    /> -->
    <!-- <TaskItem v-bind:task-list-prop="taskList" /> -->

    <ProductCard :productList="productList" />
  </div>
</template>
<style lang="css">
.card {
  display: flex;
  flex-direction: column;
  overflow: auto;
  padding-top: 5%;
  padding-bottom: 5%;
  padding-left: 15%;
  padding-right: 15%;
  gap: 5%;
  background-color: #00ab67;
  /* height: 80vh; */
  /* width: 100%; */
}
</style>
