<template>
  <!-- Section 1 -->
  <section class="w-full px-6 pb-12 antialiased bg-white">
    <div class="mx-auto max-w-8xl">
      <Nuxt />
      <TheFooter />
    </div>
  </section>
</template>

<script>
import TheFooter from "../components/TheFooter.vue";

export default {
  component: {
    TheFooter,
  },
};
</script>

<style></style>
