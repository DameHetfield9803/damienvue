<script setup>
import HomePage from "./components/HomePage.vue";
import HelloWorld from "./components/HelloWorld.vue";
import PersonalSetup from "./components/PersonalSetup.vue";
import NotFoundView from "./components/NotFound.vue";
import ForbiddenView from "./components/ForbiddenView.vue";
import { ref, computed } from "vue";

const routes = {
  "/": HomePage,
  "/hello": HelloWorld,
  "/PersonalSetup": PersonalSetup,
  "/HelloWorld": HelloWorld,
  "/:pathMatch(.*)*": NotFoundView,
  "/Forbidden": ForbiddenView,
};

const currentPath = ref(window.location.hash);

window.addEventListener("hashchange", () => {
  currentPath.value = window.location.hash;
});

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || "/"] || NotFoundView;
});
</script>

<template>
  <component :is="currentView" />
  <ul class="nav mt-3 font-mono bg-slate-950 text-violet-500 antialiased">
    <li><a href="#/">Home</a></li>
    <li><a href="#/HelloWorld">Example</a></li>
    <li><a href="#/PersonalSetup">Personal Setup</a></li>
  </ul>
</template>

<style>
.nav {
  list-style-position: inside;
  list-style-type: lower-greek;
  text-align: center;
  border-radius: 4rem;
  max-width: 15rem;
  margin: auto;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
