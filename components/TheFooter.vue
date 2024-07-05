<template>
  <footer class="bg-grey-1">
    <div class="wrapper flex flex-col sm:flex-row sm:items-center justify-between gap-y-2 py-5 sm:py-10">
      <ULink to="/" class="font-black text-xs sm:text-sm md:text-base lg:text-lg tracking-tighter uppercase font-roboto">{{ translations['logo.title'] }}</ULink>
      <p class="text-sm sm:text-base">{{ translations['footer.title'] }}</p>
    </div>
  </footer>
</template>

<script setup>
defineProps(['translations']);
</script>
