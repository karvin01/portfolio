<template>
  <div class="col-span-4 md:col-span-12 mb-1 mt-10">
    <h2 class="text-3xl md:text-4xl font-black uppercase tracking-widest text-white">
      <span class="text-main">//</span> {{ title }}
    </h2>
    <div class="h-1 w-20 bg-main mt-2 shadow-[0_0_15px_rgba(6,182,212,0.8)]"></div>
  </div>
</template>

<script setup>
// Definujeme "props", tedy proměnné, které do komponenty posíláme zvenčí
defineProps({
  title: {
    type: String,
    required: true
  }
});
</script>
