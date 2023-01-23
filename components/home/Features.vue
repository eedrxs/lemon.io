<template>
  <section class="features">
    <div class="container features-wrapper">
      <div
        v-for="{ title, iconUrl } in features"
        :key="title"
        class="features__feature"
      >
        <div class="features__feature--img">
          <img :src="iconUrl" alt="title" />
        </div>
        <div class="features__feature--title">
          <h4>{{ title }}</h4>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
const features = [
  {
    title: "Miraculous 24-hr Match",
    iconUrl: "/images/home/icon-match-guarantee.svg",
  },
  {
    title: "Custom Assisted Matching",
    iconUrl: "/images/home/icon-custom-assisted-matching.svg",
  },
  {
    title: "Zero-Risk Replacement Guarantee",
    iconUrl: "/images/home/icon-zero-risk-replacement.svg",
  },
];
</script>

<style lang="scss" scoped>
h4 {
  margin: 0;
}
.features {
  padding: 2.1875rem 0;

  &-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  &__feature {
    &--img {
      height: 5.9375rem;
      margin-left: 2.8125rem;
      margin-bottom: 0.3rem;
      img {
        max-height: 100%;
      }
    }

    &--title {
      max-width: 250px;
      h4 {
        font: 2rem "DIN Condensed Bold";
        line-height: 1.25;
      }
    }
  }
}

@media (min-width: $md-screen) {
  .features {
    &-wrapper {
      flex-direction: row;
    }

    &__feature {
      &--img {
        height: 7.8125rem;
        margin-bottom: 1.5625rem;
      }
    }
  }
}
</style>
