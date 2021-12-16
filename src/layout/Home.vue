<template>
  <section id="home" class="section section-home">
    <div class="container">
      <div class="home">
        <div class="info">
          <h2 class="info__heading">frontend-developer.</h2>
          <p class="info__desc">Hi! I'm Liliya Voloshina, a passionate Front-end Developer based in Kazakhstan.</p>
        </div>
        <div class="photo">
          <img class="photo__img" src="../assets/img/me.png" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {}
  },
  mounted() {},
  methods: {}
}
</script>

<style lang="scss">
.section-home {
  padding-top: 80px;
  background: var(--bg-dark);
}

.home {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap-reverse;
  height: 100vh;

  @media (max-width: 420px) {
    align-items: unset;
  }
}

.info {
  flex: 1 1 50%;

  &__heading {
    font-size: 5rem;
    font-weight: 900;
    letter-spacing: -0.02em;
    line-height: 1.05;
    font-family: var(--font-heading);
    color: var(--black);
  }

  &__desc {
    font-family: var(--font-base);
    line-height: 4rem;
    font-size: 1.8rem;
    color: var(--grey);
  }

  @media (max-width: 420px) {
    &__heading {
      font-size: 3rem;
    }

    &__desc {
      line-height: 3rem;
      font-size: 1.5rem;
    }
  }
}

.photo {
  flex: 1 1 500px;

  &__img {
    width: 100%;
    height: 100%;
    max-height: 500px;
    object-fit: contain;
  }
}
</style>