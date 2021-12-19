<template>
  <section id="about" class="section section-about">
    <div class="container">
      <div class="about">
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
  name: 'About',
  data() {
    return {}
  },
  mounted() {},
  methods: {}
}
</script>

<style lang="scss">
.section-about {
  background: var(--bg-dark);
}

.about {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: calc(100vh - 80px);
  margin-top: 80px;

  @media (max-width: 768px) {
    flex-direction: column;
    justify-content: center;
    row-gap: 40px;
  }
}

.info {
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

  @media (max-width: 1024px) {
    &__heading {
      font-size: 3.5rem;
    }

    &__desc {
      line-height: 3.5rem;
      font-size: 2rem;
    }
  }

  @media (max-width: 768px) {
    order: 2;

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
  &__img {
    width: 100%;
    height: 100%;
    min-width: 250px;
    max-height: 500px;
    object-fit: contain;
  }

  @media (max-width: 768px) {
    order: 1;
  }
}
</style>