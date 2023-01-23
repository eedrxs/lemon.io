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
    img {
      max-width: 345px;
    }
  }

  &__copy {
    font-family: "DIN Condensed Bold";

    &--main {
      font-size: 3rem;
      line-height: 1.13;
      letter-spacing: 0.1875rem;
      margin: 0;
      margin-bottom: 0.9375rem;
      text-transform: uppercase;
    }

    &--sub {
      font-size: 1.5625rem;
      line-height: 1.2;
      letter-spacing: 0.125rem;
      margin: 0;
      margin-bottom: 1.5625rem;
      text-transform: uppercase;
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
</style>
