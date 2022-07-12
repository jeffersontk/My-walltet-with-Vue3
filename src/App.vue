<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header/index.vue";
</script>

<template>
  <Header />
</template>

<style>
:root {
  --background: #f0f2f5;
  --shape: #ffffff;

  --red: #e52e4d;
  --blue: #5429cc;
  --blue-light: #6933ff;
  --gray-dark: #1e1e1d;
  --green: #33cc95;

  --text-title: #363f5f;
  --text-body: #969cb3;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  background: var(--background);
  -webkit-font-smoothing: antialiased;
}
</style>
