<style lang="scss" scoped>
a {
  padding: 0.9375rem 1.25rem;
  background: url("/images/yellow-button-bg.svg") 0 0/100% 100% no-repeat;
  font: 1.0625rem "Source Code Pro";
  color: $black;
  cursor: pointer;
  text-decoration: none;
  text-transform: lowercase;
  text-align: center;

  &:hover {
    background: url("/images/lemon-button-bg.svg") 0 0/100% 100% no-repeat;
  }
}

@media (min-width: $md-screen) {
  a {
    font-size: 1.125rem;
    padding: 1.25rem 2.5rem;
  }
}
</style>

<template>
  <NuxtLink :to="url"><slot /></NuxtLink>
</template>

<script lang="ts" setup>
defineProps<{
  url: string;
}>();
</script>
