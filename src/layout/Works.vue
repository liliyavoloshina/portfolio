<template>
  <section id="works" class="section section-works">
    <div class="container">
      <h3 class="section-works__title">Selected projects</h3>
      <div v-if="works" class="works">
        <CardWork v-for="work in works" :key="work.id" :work="work" />
      </div>
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

  // methods: {
  //   async getWorks() {
  //     const req = await fetch('works.json')
  //     const res = await req.json()
  //     this.works = res
  //   }
  // },

  async created() {
    const req = await fetch('works.json')
    const res = await req.json()
    this.works = res
  },
  methods: {}
}
</script>

<style lang="postcss">
.section-works__title {
  font-size: 2rem;
  font-weight: 700;
}
</style>