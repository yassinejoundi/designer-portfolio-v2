<template>
  <div id="foot">
    <div class="container py-16 md:py-20 flex flex-col lg:flex-row">
      <div
        class="w-full border-l-2 border-t-2 border-r-2 border-b-2 border-grey-60 px-6 py-6 sm:py-8 lg:w-1/2"
        v-for="info in infos"
        :key="info.id"
      >
        <div class="flex items-center">
          <i :class="`mdi mdi-${info.icon} text-2xl text-grey-40`"></i>
          <p class="pl-2 font-body font-bold uppercase text-grey-40 lg:text-lg">
            My {{ info.title }}
          </p>
        </div>
        <p class="pt-2 text-left font-body font-bold text-primary lg:text-lg">
          {{ info.content }}
        </p>
      </div>
    </div>

    <div class="bg-primary">
      <div class="container flex flex-col justify-between py-6 sm:flex-row">
        <p class="text-center font-body text-white md:text-left">
          © 2022 CopyRight By
          <a href="https://www.linkedin.com/in/yassinejoundi">Joundi Yassine</a
          >.
        </p>
        <div
          class="flex items-center justify-center pt-5 sm:justify-start sm:pt-0"
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
</template>

<script>
export default {
  data() {
    return {
      infos: [
        {
          title: 'Phone',
          icon: 'phone',
          content: '(+212) 612 345 789',
        },
        {
          title: 'Email',
          icon: 'send',
          content: 'name@email.com',
        },
      ],
      socials: this.$store.state.data.socials,
    }
  },
}
</script>

<style></style>
