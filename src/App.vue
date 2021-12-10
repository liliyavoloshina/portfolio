<template>
  <Header />
  <Home />
  <Works />
</template>

<script>
import Header from './layout/Header.vue'
import Home from './layout/Home.vue'
import Works from './layout/Works.vue'
export default {
  name: 'App',
  components: { Header, Home, Works }
}
</script>

<style>
:root {
  --black: #000;
  --bg-dark: #f8f8f8;
  --bg-light: #fff;
  --grey: #474747;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: var(--black);
}

body {
  font-family: 'Cabin', sans-serif;
  background: var(--bg-dark);
}

a {
  text-decoration: none;
}

ul {
  list-style-type: none;
}

.container {
  max-width: 1440px;
  margin-left: auto;
  margin-right: auto;
}
</style>