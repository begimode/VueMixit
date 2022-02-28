<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/Landing.vue'
import Landing from './components/Landing.vue';
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
</script>


<template>
<div>
    <header>
    <Header></Header>
  </header>
  <div>
    <!-- <Landing></Landing> -->
  </div>

  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <!-- <Landing msg="Hello Vue 3 + Vite" /> -->

  <footer>
    <!-- <Footer></Footer> -->
  </footer>
</div>

</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
