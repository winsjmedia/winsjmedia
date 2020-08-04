<template>
  <div class="home">
    <Header />
    <main class="main">
      <Nav />
      <About />
      <Blog />
      <Passions />
      <Contact />
      <Footer />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Nav from "@/components/Nav.vue";
import About from "@/components/About.vue";
import Blog from "@/components/Blog.vue";
import Passions from "@/components/Passions.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Nav,
    About,
    Blog,
    Passions,
    Contact,
    Footer,
  },
};
</script>

<style lang="scss">
.home {
  display: grid;
  grid-template-areas:
    "header"
    "main";
}
.header {
  grid-area: header;
  height: 100vh;
  overflow: hidden;
}
.googlemaps {
  width: 100%;
  height: 500px;
}
.main {
  > *:not(:last-child) {
    margin-bottom: 5rem;
  }
  grid-area: main;
  height: 100vh;
  overflow-y: scroll;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}
.main::-webkit-scrollbar {
  display: none;
}
@media only screen and (min-width: 992px) {
  .home {
    grid-template-areas: "main header";
    grid-template-columns: 50vw 50vw;
  }
}
</style>