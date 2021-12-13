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
  --font-base: 'Cabin', sans-serif;
  --font-base: 'Raleway', sans-serif;
  --font-heading: 'Raleway', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: var(--black);
}

body {
  font-family: var(--font-base);
  line-height: 1.5;
  font-weight: 400;
  background: var(--bg-dark);
}

h1,
h2,
h3 {
  font-weight: 700;
  font-family: var(--font-heading);
  letter-spacing: -1px;
}

h2 {
  font-size: 3rem;
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
  padding: 0 2rem;
}
</style>