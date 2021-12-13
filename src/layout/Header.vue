<template>
  <header class="header-wrapper">
    <div class="container header">
      <nav class="nav">
        <ul class="nav__list">
          <li class="nav__item">
            <a href="#home" class="nav__link">Home</a>
          </li>
          <li class="nav__item">
            <a href="#about" class="nav__link">About</a>
          </li>
          <li class="nav__item">
            <a href="#works" class="nav__link">Works</a>
          </li>
          <li class="nav__item">
            <a href="#contact" class="nav__link">Contact</a>
          </li>
        </ul>
      </nav>
    </div>
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

<style lang="scss" scoped>
.header-wrapper {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 10;
  background: var(--bg-light);
}

.header {
  display: flex;
  justify-content: flex-end;
}

.nav {
  flex: 1 1 100%;

  &__list {
    display: flex;
    justify-content: space-between;
  }

  &__item {
    font-size: 1.4rem;
    font-weight: 400;
  }

  &__link {
    display: block;
    padding: 1.4rem 1rem;

    &:hover {
      color: green;
    }
  }

  @media (min-width: 768px) {
    flex: 0 1 40%;
  }
}
</style>