<!--Create a component called Hello World-->
<script setup>
import { ref } from "vue";
import logo from "@/assets/logo.png";
const names = ref([
  { id: 1, name: "Damien" },
  { id: 2, name: "Daniel" },
  { id: 3, name: "En Quan" },
  { id: 4, name: "Firdaus" },
]);
</script>

<template>
  <h1>Ideation for your future websites</h1>
  <div class="div1">
    <br />
    <ul>
      <li v-for="n in names" :key="n.id"><strong>Hello</strong> {{ n.name }}</li>
    </ul>
    <br />
  </div>
  <div class="intro">
    <p>This is a website created using vue 3.0 and tailwind css</p>
    <img :src="logo" alt="Vue logo" class="rounded-sm" />
  </div>
</template>

<style scoped>
.div1 {
  text-align: left;
  color: limegreen;
}

.intro {
  color: palevioletred;
  background-color: black;
  border-radius: 1rem;
}
</style>
