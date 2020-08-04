<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import "@/assets/_variable.scss";
* {
  margin: 0;
  border: 0;
  padding: 0;
}
p,
input,
textarea {
  font-family: "Montserrat", sans-serif;
  font-size: 1.6rem;
  margin-bottom: 1rem;
  color: gray;
}
a {
  color: $primary-color;
}
.title {
  font-family: "Oswald", sans-serif;
  font-size: 2.9rem;
  margin-bottom: 1rem;
  color: black;
  font-weight: 600;
  text-transform: uppercase;
}
.highlight {
  background-color: $secondary-color;
  padding: 0 0.5rem;
  color: $primary-color;
}
html {
  font-size: 62.5%;
}
input:focus,
textarea:focus {
  outline: none;
}
input,
textarea {
  background-color: $secondary-color;
  color: gray;
  box-sizing: border-box;
  margin-bottom: 1rem;
  border-radius: 0.5rem;
  padding: 1rem;
  display: inline-block;
  width: 100%;
}
textarea {
  resize: none;
  height: 150px;
}
input[type="submit"] {
  background-color: $primary-color;
  color: white;
}
input[type="submit"]:hover {
  background-color: darken($primary-color, 10%);
}
input[type="submit"]:active {
  background-color: darken($primary-color, 20%);
}
.ohnohoney {
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
  height: 0;
  width: 0;
  z-index: -1;
}
</style>