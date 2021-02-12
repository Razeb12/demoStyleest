<template>
  <div id="app">
    <HelloWorld/>
    <Hero/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Hero from './components/Hero.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Hero,
    Main,
    Footer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
:root {
  --white: #fff;
  --black: #222;
  --pink: #f60091;
  --grey: #444;
  --grey2: #959595;
  --grey-alt: #d1e2e9;
  --yellow: #ffd800;
  --green: #59b210;
}

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  scroll-behavior: smooth;
  box-sizing: border-box;
  font-size: 62.5%;
}

body {
  position: relative;
  font-family: "Poppins", sans-serif;
  font-size: 1.6rem;
  font-weight: 400;
  color: var(--black);
  background-color: var(--white);
  z-index: -1;
}

li,
ul {
  list-style-type: none;
}

a {
  text-decoration: none;
}



</style>
