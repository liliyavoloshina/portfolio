<template>
  <Header />
  <Home />
  <Works />
  <Footer />
</template>

<script>
import Header from './layout/Header.vue'
import Home from './layout/Home.vue'
import Works from './layout/Works.vue'
import Footer from './layout/Footer.vue'
export default {
  name: 'App',
  components: { Header, Home, Works, Footer }
}
</script>

<style lang="scss">
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

html {
  font-size: 16px;

  @media (max-width: 768px) {
    font-size: 14px;
  }
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

h3 {
  font-size: 2.5rem;
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