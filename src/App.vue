<template>
  <div>
    <Navbar :logo="logo_src" :alt="app_name" />
    <RouterView />
    <Footer />
  </div>
</template>

<script>
  import { RouterView } from 'vue-router'
  import Navbar from './components/Navbar.vue'
  import Footer from './components/Footer.vue'

  export default {
    name: 'App',
    components: {
      Navbar,
      RouterView,
      Footer
    },
    data() {
      return {
        logo_src: "/images/logo.png",
        app_name: "Make your Burger"
      }
    }
  }
</script>

<style>
  * {
    font-family: "Helvetica";
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container {
    margin: 50px;
    min-height: 450px;
  }

  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>
