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
  <h1 class="intro1">Ideation for your future websites</h1>
  <div class="div1">
    <br />
    <ul>
      <li v-for="n in names" :key="n.id"><strong>Hello</strong> {{ n.name }}</li>
    </ul>
    <br />
  </div>
  <br />
  <div class="intro">
    <p>This is a website created using vue 3.0 and tailwind css</p>
    <img :src="logo" alt="Vue logo" class="vuelogo" />
  </div>
</template>

<style scoped>
.intro1 {
  color: paleturquoise;
  background-color: black;
  border-radius: 1.4rem;
  padding-left: 38rem;
  padding-right: 38rem;
  margin-bottom: 2rem;
  display: flex;
}

.div1 {
  color: limegreen;
  background-color: black;
  padding-left: 8rem;
  border-radius: 1.4rem;
  margin-top: 2rem;
  max-height: 8rem;
  max-width: 23rem;
  margin: 0 auto;
}

.vuelogo {
  width: 10rem;
  height: 10rem;
  margin: 0 auto;
  display: flex;
  margin-top: 1.2rem;
}

.div1 {
  text-align: left;
  color: limegreen;
}

.intro {
  color: palevioletred;
  margin-top: 1rem;
  background-color: black;
  border-radius: 1.4rem;
  max-width: 28rem;
  margin: 0 auto;
}
</style>
