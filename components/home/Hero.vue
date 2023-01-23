<template>
  <section class="hero">
    <div class="hero__img">
      <img
        src="/images/home/illustration-hero-main.webp"
        alt="illustration-hero-main"
      />
    </div>

    <div class="hero__copy">
      <div>
        <h1 class="hero__copy--main">Behold! The almighty devs</h1>
        <p class="hero__copy--sub">you’ve been searching for</p>
      </div>

      <p class="hero__copy--offer">
        // Why squander time and money on developers who aren’t perfect for your
        startup? Let Lemon match you with engineers that can transform your
        vision into reality — diabolically fast
      </p>

      <div class="hero__copy--lemon-button-wrapper">
        <CommonSquigglyButton url="/magic-box"
          >match me with a dev</CommonSquigglyButton
        >
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  display: flex;
  flex-direction: column;
  margin: 1.25rem 0;

  &__img {
    margin-bottom: 0.9375rem;
    max-width: 21.5625rem;
    img {
      max-width: 100%;
    }
  }

  &__copy {
    font-family: "DIN Condensed Bold";

    &--main {
      font-size: 3rem;
      line-height: 1.13;
      letter-spacing: 0.1875rem;
      text-transform: uppercase;
      margin: 0;
      margin-bottom: 0.9375rem;
    }

    &--sub {
      font-size: 1.5625rem;
      line-height: 1.2;
      letter-spacing: 0.125rem;
      text-transform: uppercase;
      margin: 0;
      margin-bottom: 1.5625rem;
    }

    &--offer {
      font: 300 1rem/1.63 "Source Code Pro";
      max-width: 31.25rem;
      margin: 0;
      margin-bottom: 1.875rem;
    }

    &--lemon-button-wrapper {
      display: flex;
      justify-content: center;
    }
  }
}

@media (min-width: $md-screen) {
  .hero {
    flex-direction: row-reverse;
    margin: 2.5rem 0;

    &__img {
      padding-top: 9.375rem;
    }

    &__copy {
      &--main {
        font-size: 7rem;
        line-height: 1.07;
        letter-spacing: 0.4rem;
        margin-top: 0.5rem;
        margin-bottom: 0.3125rem;
      }

      &--sub {
        font-size: 3.5rem;
        line-height: 1;
        letter-spacing: 0.3125rem;
        margin-bottom: 2.1875rem;
      }

      &--offer {
        font-size: 1.125rem;
        line-height: 1.56;
        margin-bottom: 3.125rem;
      }

      &--lemon-button-wrapper {
        justify-content: start;
      }
    }
  }
}
</style>
