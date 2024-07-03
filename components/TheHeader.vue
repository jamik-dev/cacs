<template>
  <header id="header" class="sticky top-0 z-10 bg-white">
    <div class="wrapper flex items-center justify-between py-8">
      <div class="flex items-center gap-6">
        <ULink to="/" class="font-[1000] text-lg tracking-tighter uppercase font-roboto"> Central Asia Container Service </ULink>
        <div class="w-[1px] bg-grey-4 h-6 shrink-0"></div>
        <nav>
          <ul class="flex items-center gap-10">
            <li><ULink to="#about">About us</ULink></li>
            <li><ULink to="#contacts">Contacts</ULink></li>
            <li><ULink to="#services">Services</ULink></li>
          </ul>
        </nav>
      </div>
      <div class="flex items-center gap-6">
        <div class="spce-y-1">
          <p class="text-grey-0 text-sm">E-mail</p>
          <a class="font-medium" href="mailto:info@cacs.hk" target="_blank">info@cacs.hk</a>
        </div>
        <div class="w-[1px] bg-grey-4 h-10"></div>
        <div class="spce-y-1">
          <p class="text-grey-0 text-sm">E-mail</p>
          <a class="font-medium" href="mailto:projects@cacs.hk" target="_blank">projects@cacs.hk</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
// eventListeners
onMounted(() => {
  if (process.client) {
    const header = document.querySelector('#header');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 108) {
        header.classList.add('shadow-lg');
      } else if (window.scrollY <= 108) {
        header.classList.remove('shadow-lg');
      }
    });
  }
});

onUnmounted(() => {
  if (process.client) {
    window.removeEventListener('scroll', () => {
      if (window.scrollY > 108) {
        header.classList.add('shadow-lg');
      } else if (window.scrollY <= 108) {
        header.classList.remove('shadow-lg');
      }
    });
  }
});
</script>
