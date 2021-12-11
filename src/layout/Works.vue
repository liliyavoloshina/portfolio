<template>
  <section id="works" class="section section-works">
    <div class="section-works__heading container">
      <h3 class="section-works__title">Selected projects.</h3>
      <p class="section-works__desc">Since starting programming as a freelancer nearly 1 years ago I've created a lot of
        projects</p>
    </div>
    <div v-if="works" class="works">
      <CardWork v-for="work in works" :key="work.id" :work="work" />
    </div>
  </section>
</template>

<script>
import CardWork from '../components/CardWork.vue'

export default {
  name: 'Home',
  components: { CardWork },
  data() {
    return {
      works: []
    }
  },

  async created() {
    const req = await fetch('works.json')
    const res = await req.json()
    this.works = res
  },
  methods: {}
}
</script>

<style lang="postcss">
.section-works {
  background: var(--bg-light);

  &__heading {
    display: flex;
    flex-direction: column;
    padding: 5rem;
    align-items: center;
  }

  &__title {
    a
    font-size: 2rem;
    font-weight: 700;
    font-family: var(--font-heading);
  }

  &__desc {
    font-size: 1.4rem;
    color: var(--grey);
  }
}
</style>
