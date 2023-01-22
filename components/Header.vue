<template>
  <div class="header-wrapper">
    <header class="header">
      <div class="header__sidebar"><Sidebar /></div>

      <div class="header__logo">
        <img src="/images/logo-lemon@2x.png" alt="lemon company logo" />
      </div>

      <nav class="header__links">
        <ul>
          <li><NuxtLink to="/blog">blog</NuxtLink></li>
          <li><NuxtLink to="/for-devs">for devs</NuxtLink></li>
          <li><NuxtLink to="/about-us">about us</NuxtLink></li>
          <li><NuxtLink to="/resources">resources</NuxtLink></li>

          <li class="header__links--apply-button">
            <NuxtLink>apply as dev</NuxtLink>
          </li>

          <li class="header__links--hire-button">
            <NuxtLink>hire talent</NuxtLink>
          </li>

          <li><NuxtLink>login</NuxtLink></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px 0;

  &-wrapper {
    margin: auto;
    max-width: $content-width;
    padding: 0 $content-padding;
  }

  &__logo img {
    width: 195px;
  }

  &__links {
    display: none;
    font: 300 1.0625rem "Source Code Pro";
    width: 795px;

    ul {
      margin: 0;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    li {
      height: 2.5rem;
      display: inline-flex;
      align-items: center;
      transition: all 0.1s;
    }

    li:not(&--apply-button):not(&--hire-button) {
      a {
        text-decoration: none;
        color: $white;
      }

      :hover {
        color: $yellow;
      }

      ::after {
        content: "/";
        margin-left: 8px;
        visibility: hidden;
        color: $yellow;
      }

      :hover::after {
        visibility: visible;
      }
    }

    &--apply-button {
      @include nav-button(#c58fff, outline);
    }

    &--hire-button {
      @include nav-button($lemon, fill);
    }
  }
}

@media (min-width: $lg-screen) {
  .header {
    justify-content: space-between;

    &__sidebar {
      display: none;
    }

    &__links {
      display: flex;
    }
  }
}
</style>
