<template>
  <div class="hero-section relative bg-cover bg-center bg-no-repeat py-8">
    <div
      class="absolute inset-0 z-20 bg-gradient-to-r from-hero-gradient-from to-hero-gradient-to bg-cover bg-center bg-no-repeat"
    ></div>

    <div
      class="container relative z-30 pt-20 pb-12 sm:pt-56 sm:pb-48 lg:pt-64 lg:pb-48"
    >
      <div class="flex flex-col items-center justify-center lg:flex-row">
        <div class="rounded-full border-8 border-primary shadow-xl">
          <img
            :src="require('@/static/img/author.jpg')"
            class="h-48 w-52 rounded-full sm:h-56 bg-cover bg-center"
            alt="author"
          />
        </div>
        <div class="pt-8 sm:pt-10 lg:pl-8 lg:pt-0">
          <h1
            class="text-center font-header text-4xl text-white sm:text-left sm:text-5xl md:text-6xl"
          >
            Hello I'm {{ name }}!
          </h1>
          <div
            class="flex flex-col justify-center pt-3 sm:flex-row sm:pt-5 lg:justify-start"
          >
            <div
              class="flex items-center justify-center pl-0 sm:justify-start md:pl-1"
            >
              <p class="font-body text-lg uppercase text-white">
                Let's connect
              </p>
              <div class="hidden sm:block">
                <i class="mdi mdi-chevron-right text-3xl text-yellow"></i>
              </div>
            </div>
            <div
              class="flex items-center justify-center pt-5 pl-2 sm:justify-start sm:pt-0"
            >
              <a v-for="social in socials" :key="social.id" :href="social.link">
                <i
                  :class="`mdi mdi-${social.icon} text-2xl text-white hover:text-yellow mx-2`"
                ></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: this.$store.state.data.name,
      socials: this.$store.state.data.socials,
    }
  },
}
</script>

<style scoped>
.hero-section {
  background-image: url(@/static/img/bg-hero.jpg);
}
</style>
