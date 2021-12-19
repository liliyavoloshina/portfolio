<template>
  <header class="header-wrapper">
    <div class="container header">
      <nav class="nav">
        <ul class="nav__list">
          <li class="nav__item">
            <a href="#about" class="nav__link underline-effect">About</a>
          </li>
          <li class="nav__item">
            <a href="#works" class="nav__link underline-effect">Works</a>
          </li>
          <li class="nav__item">
            <a href="#contact" class="nav__link underline-effect">Contact</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
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
  box-shadow: 0 1px 4px -2px rgba(0, 0, 0, 0.2);
}

.header {
  display: flex;
  justify-content: flex-end;

  &.container {
    padding: 0;
  }
}

.nav {
  flex: 1 1 100%;

  &__list {
    display: flex;
    justify-content: space-between;
  }

  &__item {
    position: relative;
    flex: 1 1;
    text-align: center;
    font-size: 1.2rem;
    font-weight: 400;
  }

  &__link {
    display: block;
    padding: 1rem 0.5rem;

    &:hover {
      color: var(--accent);
    }
  }

  @media (min-width: 768px) {
    flex: 0 1 25%;

    &__item {
      font-size: 1.4rem;
    }

    &__link {
      padding: 1.4rem 1rem;
    }
  }
}
</style>