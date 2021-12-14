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
          <div class="photo__circle"></div>
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
  background: var(--bg-dark);
}

.home {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap-reverse;
  height: 100vh;
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
  position: relative;
  /* flex: 1 1 500px; */
  /* width: 500px; */
  /* height: 500px; */

  &__img {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 2;
    margin: auto;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  &__circle {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 450px;
    height: 450px;
    background: var(--bg-light);
    border-radius: 50%;

    margin: auto;
    z-index: 1;
  }
}
</style>