<template>
  <article class="work-wrapper">
    <div class="work container">
      <div class="work__info">
        <h2 class="work__title">{{work.title}}</h2>
        <p class="work__desc">{{work.desc}}</p>
        <ul class="stack">
          <li v-for="stack in work.stack" :key="stack" class="stack__item">{{stack}}</li>
        </ul>
        <div class="work__links">
          <a v-if="work.codeUrl" :href="work.codeUrl" class="work__link">Code</a>
          <a :href="work.liveUrl" class="work__link">Live</a>
        </div>
      </div>
      <div class="work__img">
        <img :src="`/src/assets/img/${work.id}.png`" :alt="work.title">
      </div>
    </div>
  </article>
</template>

<script>
export default {
  props: ['work'],
  name: 'Work'
}
</script>

<style lang="scss">
.work-wrapper {
  background: var(--bg-dark);
  padding: 2rem 0;
}

.work {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;

  &__info {
    flex: 1 1 400px;
    max-width: 500px;
    display: flex;
    flex-direction: column;
    gap: 1.3rem;
  }

  &__desc {
    white-space: pre-line;
  }

  &__links {
    display: flex;
    gap: 1rem;
  }

  &__link {
    font-weight: 700;
  }

  &__img {
    width: 600px;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  @media (max-width: 768px) {
    flex-direction: column;
    align-items: initial;
    gap: 2rem;

    &__info {
      flex: 1 1 200px;
      order: 2;
    }

    &__img {
      width: 100%;
    }
  }
}

.stack {
  display: flex;
  gap: 1rem;

  &__item {
  }
}
</style>