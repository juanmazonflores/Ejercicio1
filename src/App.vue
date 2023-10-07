<template>
  <Navbar/>
  <Home/>
  <Intro/>
  <Directivas/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Intro from './components/Intro.vue'
import Directivas from './components/Directivas.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    Intro,
    Directivas
  }
}
</script>

<style>
  @import "../public/css/style.css";
</style>
