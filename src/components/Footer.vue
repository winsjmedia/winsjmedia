<template>
  <div class="footer">
    <p class="footer__title title">
      <span class="highlight">Winsj</span> Media
    </p>
    <div class="footer__social-media">
      <i class="fa fa-facebook-square fa-4x" aria-hidden="true"></i>
      <i class="fa fa-twitter-square fa-4x" aria-hidden="true"></i>
      <i class="fa fa-youtube-square fa-4x" aria-hidden="true"></i>
      <i class="fa fa-soundcloud fa-4x" aria-hidden="true"></i>
      <i class="fa fa-github-square fa-4x" aria-hidden="true"></i>
    </div>
    <p>© 2020 Copyright WinsjMedia. All rights reserved.</p>
    <p>
      Developed by
      <a href="#">WinsjMedia</a>
    </p>
    <div v-on:click="up" class="footer__up">
      <i class="fa fa-arrow-up fa-2x" aria-hidden="true"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  methods: {
    up: function () {
      window.scrollTo(0, 0);
      console.log("upping");
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/_variable.scss";
.footer {
  &:before {
    background: inherit;
    top: 0;
    content: "";
    display: block;
    height: 100%;
    left: 0;
    position: absolute;
    right: 0;
    transform: skewY(5deg);
    transform-origin: 100%;
    z-index: -1;
  }
  position: relative;
  text-align: center;
  background-color: $primary-color;
  padding: 2.5rem 0;
  a,
  i,
  p {
    color: white;
  }
  &__title {
    color: white;
  }
  &__social-media {
    display: flex;
    justify-content: center;
    margin: 2rem 0;
    * {
      margin-left: 10px;
    }
  }
  &__up {
    position: absolute;
    left: 2.5rem;
    top: 2.5rem;
    background-color: $secondary-color;
    height: 43px;
    width: 43px;
    box-sizing: border-box;
    padding: 0 1rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    transition: all 0.3s ease-in-out 0s;
    &:hover {
      i {
        cursor: default;
        transform: rotate(360deg);
        transition: all 0.3s ease-in-out 0s;
      }
    }
    i {
      color: $primary-color;
    }
  }
}
@media only screen and (min-width: 992px) {
  .footer {
    margin-top: 12rem !important;
  }
}
</style>