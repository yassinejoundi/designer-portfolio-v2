<template>
  <div class="home">
    <Hero />
    <About />
    <Services />
    <Portfolio />
    <Statistics />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import About from '~/components/About'
import Services from '~/components/Services'
import Portfolio from '~/components/Portfolio'
import Statistics from '~/components/Statistics'
export default {
  name: 'IndexPage',
  components: { Hero, About, Services, Portfolio, Statistics },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@1,500');

* {
  padding: 0;
  margin: 0;
  font-family: 'Nunito', sans-serif;
  box-sizing: border-box;
}
</style>
