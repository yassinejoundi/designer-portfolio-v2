<template>
  <div class="container py-16 md:py-20" id="services">
    <h2
      class="text-center font-header text-4xl font-semibold uppercase text-primary sm:text-5xl lg:text-6xl"
    >
      Here's what I'm good at
    </h2>
    <h3
      class="pt-6 text-center font-header text-xl font-medium text-black sm:text-2xl lg:text-3xl"
    >
      These are the services I offer
    </h3>

    <div
      class="grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
    >
      <div
        class="group rounded px-8 py-12 shadow hover:bg-primary"
        v-for="service in services"
        :key="service.id"
      >
        <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
          <div class="hidden group-hover:block">
            <img
              :src="require(`@/static/img/services/${service.icon}-white.svg`)"
              :alt="service.title"
            />
          </div>
          <div class="block group-hover:hidden">
            <img
              :src="require(`@/static/img/services/${service.icon}-black.svg`)"
              :alt="service.title"
            />
          </div>
        </div>
        <div class="text-center">
          <h3
            class="pt-8 text-lg font-semibold uppercase text-primary group-hover:text-yellow lg:text-xl"
          >
            {{ service.title }}
          </h3>
          <p class="text-grey pt-4 text-sm group-hover:text-white md:text-base">
            {{ service.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          title: 'WEBSITE DESIGN',
          description:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
          icon: 'web-design',
        },
        {
          title: 'GRAPHIC DESIGN',
          description:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
          icon: 'graphic-design',
        },
        {
          title: 'BRANDING',
          description:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
          icon: 'branding',
        },
      ],
    }
  },
}
</script>

<style></style>
