<template>
  <article class="card-work-wrapper">
    <div class="container">
      <div class="card-work__info">
        <h3 class="card-work__title">{{work}}</h3>
      </div>
      <div class="card-work__img"></div>
    </div>
  </article>
</template>

<script>
export default {
  props: ['work'],
  name: 'CardWork',
  data() {
    return {}
  },
  mounted() {},
  methods: {}
}
</script>

<style lang="postcss">
.card-work-wrapper {
  padding: 1rem;
  background: var(--bg-dark);

  &:hover {
    background: var(--bg-light);
  }
}
</style>