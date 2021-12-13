<template>
  <section id="works" class="section section-works">
    <div class="section-works__heading">
      <h2 class="section-works__title">Selected projects.</h2>
      <p class="section-works__desc">Since starting programming as a freelancer nearly 1 years ago I've created a lot of
        projects</p>
    </div>
    <div v-if="works" class="works">
      <Work v-for="work in works" :key="work" :work="work" />
    </div>
  </section>
</template>

<script>
import Work from '../components/Work.vue'
import data from '../assets/data/works.json'

export default {
  name: 'Home',
  components: { Work },
  data() {
    return {
      works: data
    }
  }
}
</script>

<style lang="scss">
.section-works {
  background: var(--bg-light);

  &__heading {
    padding: 10% 2rem;
  }

  &__title {
    margin-bottom: 2rem;
  }

  &__desc {
    font-size: 1.4rem;
    color: var(--grey);
  }
}
</style>
