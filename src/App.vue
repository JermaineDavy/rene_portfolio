<template>
  <div id="app">
    <Navigation></Navigation>
    <Hero></Hero>
    <Sidekick></Sidekick>

    <Testimonials></Testimonials>

    <section style="height: 400px;"></section>

    <Foot></Foot>
  </div>
</template>

<script>
import Navigation from './components/Navigation';
import Hero from './components/Hero';
import Foot from './components/Foot';
import Sidekick from './components/Sidekick';
import Testimonials from './components/Testimonials';

export default {
  name: 'App',
  components: {
    Foot,
    Navigation,
    Hero,
    Sidekick,
    Testimonials
  }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  overflow: hidden;
}
</style>
