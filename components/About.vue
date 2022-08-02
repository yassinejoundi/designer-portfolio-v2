<template>
  <div class="bg-grey-50" id="about">
    <div
      class="container flex flex-col items-center py-16 md:py-20 lg:flex-row"
    >
      <div class="w-full text-center sm:w-3/4 lg:w-3/5 lg:text-left">
        <h2
          class="font-header text-4xl font-semibold uppercase text-primary sm:text-5xl lg:text-6xl"
        >
          Who am I?
        </h2>
        <h4
          class="pt-6 font-header text-xl font-medium text-black sm:text-2xl lg:text-3xl"
        >
          I'm {{ name }}, a Graphic Designer & Photographer
        </h4>
        <p class="pt-6 font-body leading-relaxed text-grey-20">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </p>
        <div
          class="flex flex-col justify-center pt-6 sm:flex-row lg:justify-start"
        >
          <div class="flex items-center justify-center sm:justify-start">
            <p class="font-body text-lg font-semibold uppercase text-grey-20">
              Connect with me
            </p>
            <div class="hidden sm:block">
              <i class="mdi mdi-chevron-right text-2xl text-primary"></i>
            </div>
          </div>
          <div
            class="flex items-center justify-center pt-5 pl-2 sm:justify-start sm:pt-0"
          >
            <a v-for="social in socials" :key="social.id" :href="social.link">
              <i
                :class="`mdi mdi-${social.icon} text-2xl text-primary hover:text-yellow mx-2`"
              ></i>
            </a>
          </div>
        </div>
      </div>
      <div class="w-full pl-0 pt-4 sm:w-3/4 lg:w-2/5 lg:pl-12 lg:pt-0">
        <div class="pt-6" v-for="skill in skills" :key="skill.id">
          <div class="flex items-end justify-between">
            <h4 class="font-body font-semibold uppercase text-black">
              {{ skill.name }}
            </h4>
            <h3 class="font-body text-3xl font-bold text-primary">
              {{ skill.width }}%
            </h3>
          </div>
          <div class="mt-2 h-3 w-full rounded-full bg-lila">
            <div
              class="h-3 rounded-full bg-primary"
              :style="`width: ${skill.width}%`"
            ></div>
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
      skills: [
        {
          name: 'Adobe Photoshop',
          width: '85',
        },
        {
          name: 'Adobe Illustrator',
          width: '70',
        },
        {
          name: 'Sketch',
          width: '98',
        },
        {
          name: 'Adobe InDesign',
          width: '91',
        },
      ],
    }
  },
}
</script>

<style></style>
