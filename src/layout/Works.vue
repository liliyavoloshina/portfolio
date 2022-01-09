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
        <h2 class="note-section__title">You can find more in my github</h2>
        <p class="note-section__desc"><a href="https://github.com/liliyavoloshina" class="arrow-link"
            target="__blank">view all
            projects
          </a></p>
      </div>
    </div>
  </section>
</template>

<script>
import Work from '../components/Work.vue'
import data from '../data/works.json'

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

.arrow-link {
  padding: 2rem 0;
  color: inherit;
  transition: 0.3s;

  &:hover {
    color: var(--accent);
  }
}

.arrow-link:after {
  font-size: 2.5rem;
  position: relative;
  content: '\2192';
  color: var(--accent);
  bottom: -3px;
  display: inline-block;
  animation: 2s ease-in-out infinite arrow;
}

@keyframes arrow {
  0% {
    transform: translateX(0px);
  }

  50% {
    transform: translateX(10px);
  }

  100% {
    transform: translateX(0px);
  }
}
</style>
