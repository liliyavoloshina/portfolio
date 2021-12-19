<template>
  <Header />
  <About />
  <Works />
  <Footer />
</template>

<script>
import Header from './layout/Header.vue'
import About from './layout/About.vue'
import Works from './layout/Works.vue'
import Footer from './layout/Footer.vue'
export default {
  name: 'App',
  components: { Header, About, Works, Footer }
}
</script>

<style lang="scss">
:root {
  --black: #282828;
  --bg-dark: #f8f8f8;
  --bg-light: #fff;
  --grey: #474747;
  --grey-lighten: #e8e8e8;
  --accent: #ff00ff;
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
  scroll-behavior: smooth;

  @media (max-width: 768px) {
    font-size: 14px;
  }
}

body {
  font-family: var(--font-base);
  line-height: 1.5;
  font-weight: 400;
  background: var(--bg-dark);

  &::-webkit-scrollbar {
    width: 10px;
  }

  &::-webkit-scrollbar-track {
    box-shadow: inset 0 0 3px rgba(0, 0, 0, 0.2);
  }

  &::-webkit-scrollbar-thumb {
    border-radius: 4px;
    background-color: var(--black);
  }
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

::selection {
  background-color: var(--accent);
}

.container {
  max-width: 1440px;
  margin-left: auto;
  margin-right: auto;
  padding: 0 2rem;
}

.underline-effect {
  &:after {
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    bottom: 0;
    left: 0;
    background-color: var(--accent);
    transform: scaleX(0);
    transform-origin: bottom right;
    transition: transform 0.3s;
  }

  &:hover {
    &:after {
      transform-origin: bottom left;
      transform: scaleX(1);
    }
  }
}
</style>