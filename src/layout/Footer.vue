<template>
  <footer id="contact" class="footer-wrapper">
    <div class="container footer">
      <h2 class="footer__title">
        Get In Touch
      </h2>
      <p class="footer__desc">I am looking for a job where I could learn new things from professionals and work on
        interesting projects</p>
      <div class="social">
        <ul class="social__list">
          <li><a href="https://t.me/liliyavoloshina" class="social__link">
              <i class="fab fa-telegram"></i>
            </a>
          </li>
          <li><a href="mailto:liliyavoloshine@gmail.com" class="social__link">
              <i class="fas fa-at"></i>
            </a>
          </li>
          <li><a href="https://discord.com/users/733317349913919558/" class="social__link">
              <i class="fab fa-discord"></i>
            </a>
          </li>
          <li><a href="https://github.com/liliyavoloshina" class="social__link"><i class="fab fa-github"></i></a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
.footer-wrapper {
  background-color: var(--black);
}

.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10% 0;

  &__title {
    font-size: 6.5rem;
    color: var(--bg-light);

    @media (max-width: 768px) {
      font-size: 4rem;
    }
  }

  &__desc {
    font-size: 1.4rem;
    color: var(--grey);
    padding: 0 1rem;
    text-align: center;
  }
}

.social {
  padding: 5% 0;

  &__list {
    display: flex;
    gap: 1rem;
    color: var(--bg-light);
  }

  &__link {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 30px;
    height: 30px;
    padding: 2rem;
    border-radius: 100%;
    transition: 0.3s;

    i {
      font-size: 1.5rem;
      color: var(--bg-light);
      transition: 0.3s;
    }

    &:hover {
      background-color: var(--accent);
      i {
        color: var(--black);
      }
    }
  }
}
</style>