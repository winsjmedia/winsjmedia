<template>
  <div class="passions">
    <p class="passions__title title">DO WHAT YOU LOVE, AND YOU WILL NEVER WORK A DAY IN YOUR LIFE</p>
    <p class="passions__text" id="typeit"></p>
  </div>
</template>

<script>
export default {
  name: "Passions",
  mounted: function () {
    new TypeIt("#typeit", {
      waitUntilVisible: true,
      loop: true,
    })
      .type("#programming", { delay: 1000 })
      .delete()
      .type("#music", { delay: 1000 })
      .delete()
      .type("#drawing", { delay: 1000 })
      .delete()
      .type("#writing", { delay: 1000 })
      .go();
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/_variable.scss";
.passions {
  background-color: $primary-color;
  padding: 2.5rem 0;
  text-align: center;
  height: 15rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  &__title {
    color: white;
  }
  &__text {
    color: white;
    font-size: 2rem;
  }
}
</style>