<script setup>
import PageLorem from "@/components/LoremPage.vue";
</script>

<template>
  <div class="wrapper">
    <PageLorem />
  </div>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@font-face {
  font-family: "gotham-bold";
  src: url("./assets/GothamBold.ttf") format("truetype");
}
@font-face {
  font-family: "proxima-nova-regular";
  src: url("./assets/ProximaNovaRegular.ttf") format("truetype");
}
a,
.title {
  font-family: "gotham-bold";
  text-decoration: none;
  text-align: center;
  color: rgb(255, 255, 255);
  margin-bottom: 10px;
}

.description {
  font-family: "proxima-nova-regular";
  text-decoration: none;
  text-align: center;
  margin-bottom: 60px;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: flex;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
