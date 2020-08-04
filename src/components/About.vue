<template>
  <div class="about">
    <div class="about__header">
      <p class="about__title title">
        <span class="highlight">About</span>
        Me
      </p>
      <p class="about__text">
        Welcome to my little corner of the web.
        <br />
        <br />As with life this place is always under construction, but it should at all times be considered somewhat of a functional home to my ever growing randomness of content (if it can even be described as such).
        <br />
        <br />I don't have much of a roadmap for this place, but for now it seems like we are heading into a simplistic and slightly humorous enviroment.
        <br />
        <br />Who am I you ask?
        <br />
        <br />Well, I've been asking myself that for years now, so if you figure it out please let me know.
        <br />
        <br />On a bit more of a seriousness note though, I am a 28 year old man from Norway with a huge passion for anything creative. I work as a programmer making websites, programs and other things involving telling the computer what to do. I love making music and the fingers on one of my hands are constantly crossed in hopes that I can break through with it one day.
        <br />
        <br />Other than that I live a considerably normal and relaxing life (with the exception of a slightly high intake of energy drinks) in a small town, where I'm either in the middle of an exciting adventure, or trying to figure out what the next one will be.
        <br />
        <br />Enjoy your stay and feel like home, just make sure you put everything back the way it was before you leave.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped lang="scss">
@import "@/assets/_variable.scss";
.about {
  position: relative;
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
  &:after {
    background: inherit;
    bottom: 0;
    content: "";
    display: block;
    height: 100%;
    left: 0;
    position: absolute;
    right: 0;
    transform: skewY(-5deg);
    transform-origin: 100%;
    z-index: -1;
  }
  background-color: $primary-color;
  &__header {
    margin-bottom: 2.5rem;
    text-align: center;
  }
  &__title,
  &__text {
    color: white;
  }
  padding: 2.5rem;
}
@media only screen and (min-width: 992px) {
  .about {
    margin-top: 12rem !important;
    margin-bottom: 9rem !important;
  }
}
</style>