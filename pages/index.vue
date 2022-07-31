<template>
  <div class="home">
    <Hero />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
export default {
  name: 'IndexPage',
  components: { Hero },
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
