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
          <a :href="work.codeUrl" class="work__link">Code</a>
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
  padding: 2rem;
  background: var(--bg-dark);
}

.work {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;

  &__info {
    flex: 1 1 200px;
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
    height: 430px;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  @media (max-width: 768px) {
    flex-direction: column;
    gap: 2rem;

    &__info {
      order: 2;
    }

    &__img {
      width: 100%;
      height: 400px;
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