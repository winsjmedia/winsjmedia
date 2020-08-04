<template>
  <div class="header">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img
            alt="Photo by Arian Darvishi on Unsplash"
            src="../assets/arian-darvishi-wh-RPfR_3_M-unsplash.jpg"
          />
        </div>
        <div class="swiper-slide">
          <img
            alt="Photo by Kelly Sikkema on Unsplash"
            src="../assets/kelly-sikkema-o2TRWThve_I-unsplash.jpg"
          />
        </div>
        <div class="swiper-slide">
          <img
            alt="Photo by Kalen Emsley on Unsplash"
            src="../assets/kalen-emsley-Bkci_8qcdvQ-unsplash.jpg"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  mounted: function () {
    this.swiper = new Swiper(".swiper-container", {
      speed: 400,
    });
  },
};
</script>

<style scoped lang="scss">
img {
  height: 100%;
}
.swiper-container {
  height: 100%;
}
</style>