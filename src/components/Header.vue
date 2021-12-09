<template>
  <header class="header">
    <nav class="nav">
      <ul class="nav__list">
        <li class="nav__item">
          <a href="#home">Home</a>
        </li>
        <li class="nav__item">
          <a href="#about">About</a>
        </li>
        <li class="nav__item">
          <a href="#works">Corks</a>
        </li>
        <li class="nav__item">
          <a href="#contact">Contact</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {}
  },
  mounted() {},
  methods: {}
}
</script>

<style lang="postcss" scoped>
.nav {
  & .nav__list {
    background: red;
  }
}
</style>