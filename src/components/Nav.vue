<template>
  <div class="nav">
    <div class="nav__header">
      <h1 class="nav__title title">
        <span class="highlight">Winsj</span>Media
      </h1>
      <p
        class="nav__description"
      >"As I go through life I put my memories into words, so they can live on forever." - Me</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style scoped lang="scss">
.nav {
  padding: 0 2.5rem;
  text-align: center;
  margin: 5rem 0;
  &__title {
    font-size: 5rem !important;
    font-weight: 400;
  }
  &__header {
    margin-bottom: 2.5rem;
  }
  &__description {
    font-style: italic;
  }
}
</style>