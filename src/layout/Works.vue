<template>
  <section id="works" class="section section-works">
    <div class="note-section">
      <div class="container">
        <h2 class="note-section__title">Selected projects.</h2>
        <p class="note-section__desc">Since starting programming as a freelancer nearly 1 years ago I've created a lot
          of
          projects</p>
      </div>
    </div>
    <div v-if="works" class="works">
      <Work v-for="work in works" :key="work" :work="work" />
    </div>
    <div class="note-section">
      <div class="container">
        <h2 class="note-section__title">You can find more in my github repo</h2>
        <p class="note-section__desc"><a href="https://github.com/liliyavoloshina">view all projects</a></p>
      </div>
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
}

.note-section {
  padding-top: 10%;
  padding-bottom: 10%;

  &__heading {
    padding-top: 10%;
    padding-bottom: 10%;
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
