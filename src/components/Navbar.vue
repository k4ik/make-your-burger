<script>
  import { RouterLink } from 'vue-router'

  export default {
    name: "Navbar",
    components: {
      RouterLink
    },
    props: ["logo", "alt"]
  }
</script>

<template>
  <header>
    <nav id="nav">
      <RouterLink to="/" id="logo-url"><img :src="logo" :alt="alt" id="logo" /></RouterLink>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/pedidos">Pedidos</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
    #nav {
        background-color: #222;
        border-bottom: 4px solid #111;
        padding: 15px 50px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }
    
    #nav a {
        color: #fcba03;
        text-decoration: none;
        margin: 12px;
        transition: .5s;
    }

    #nav a:hover {
        color: #fff;
    }

    #nav #logo-url {
        margin: auto;
        margin-left: 0;
    }

    #logo {
        width: 40px;
    }
</style>
