<template>
  <div class="container py-16 md:py-20" id="portfolio">
    <h2
      class="text-center font-header text-4xl font-semibold uppercase text-primary sm:text-5xl lg:text-6xl"
    >
      Check out my Portfolio
    </h2>
    <h3
      class="pt-6 text-center font-header text-xl font-medium text-black sm:text-2xl lg:text-3xl"
    >
      Here's what I have done with the past
    </h3>

    <div
      class="mx-auto grid w-full grid-cols-1 gap-8 pt-12 sm:w-3/4 md:gap-10 lg:w-full lg:grid-cols-2"
    >
      <img
        v-for="i in 9"
        :key="i"
        :src="require(`@/static/img/gallery/gallery-${i}.jpg`)"
        class="w-full shadow mx-auto transform transition-all hover:scale-105 md:mx-0"
        alt="portfolio image"
      />
    </div>
    <!--
        <div
          class="mx-auto grid w-full grid-cols-1 gap-8 pt-12 sm:w-3/4 md:gap-10 lg:w-full lg:grid-cols-2"
        >
          <a
            href="/"
            class="mx-auto transform transition-all hover:scale-105 md:mx-0"
          >
            <img
              src="/assets/img/portfolio-apple.jpeg"
              class="w-full shadow"
              alt="portfolio image"
            />
          </a>
          <a
            href="/"
            class="mx-auto transform transition-all hover:scale-105 md:mx-0"
          >
            <img
              src="/assets/img/portfolio-stripe.jpeg"
              class="w-full shadow"
              alt="portfolio image"
            />
          </a>
          <a
            href="/"
            class="mx-auto transform transition-all hover:scale-105 md:mx-0"
          >
            <img
              src="/assets/img/portfolio-fedex.jpeg"
              class="w-full shadow"
              alt="portfolio image"
            />
          </a>
          <a
            href="/"
            class="mx-auto transform transition-all hover:scale-105 md:mx-0"
          >
            <img
              src="/assets/img/portfolio-microsoft.jpeg"
              class="w-full shadow"
              alt="portfolio image"
            />
          </a>
        </div>
    -->
  </div>
</template>

<script>
export default {}
</script>

<style></style>
