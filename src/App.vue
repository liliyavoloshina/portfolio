<template>
  <Header />
  <Home />
</template>

<script>
import Header from './components/Header.vue'
import Home from './components/Home.vue'
export default {
  name: 'App',
  components: { Header, Home }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Helvetica, Arial, sans-serif;
}

ul {
  list-style-type: none;
}
</style>