<template>
  <div
    class="bg-cover bg-top bg-no-repeat pb-16 md:py-16 lg:py-24"
    id="statistics"
  >
    <div class="container">
      <div
        class="mx-auto w-5/6 bg-white py-16 shadow md:w-11/12 lg:py-20 xl:py-24 2xl:w-full"
      >
        <div class="grid grid-cols-2 gap-5 md:gap-8 xl:grid-cols-4 xl:gap-5">
          <div
            class="flex flex-col items-center justify-center text-center md:flex-row md:text-left"
            v-for="state in states"
            :key="state.id"
          >
            <div>
              <img
                :src="require(`@/static/img/statisiques/${state.icon}.svg`)"
                class="mx-auto h-12 w-auto md:h-20"
                :alt="state.title"
              />
            </div>
            <div class="pt-5 md:pl-5 md:pt-0">
              <h1 class="font-body text-2xl font-bold text-primary md:text-4xl">
                {{ state.number }}
              </h1>
              <h4
                class="text-grey-dark font-header text-base font-medium leading-loose md:text-xl"
              >
                {{ state.title }}
              </h4>
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
      states: [
        {
          icon: 'brochure-catalog-icon',
          title: 'Finished Projects',
          number: '74',
        },
        {
          icon: 'satisfaction-icon',
          title: 'Happy Clients',
          number: '56',
        },
        {
          icon: 'announcement-icon',
          title: 'Brand Identity',
          number: '16',
        },
        {
          icon: 'three-stars-icon',
          title: 'Experience Years',
          number: '8',
        },
      ],
    }
  },
}
</script>

<style scoped>
#statistics {
  background-image: url(@/static/img/bg-statistics.png);
}
</style>
