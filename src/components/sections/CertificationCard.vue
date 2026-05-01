<script setup>
defineProps({
  title: String,
  desc: String,
})
</script>

<template>
  <div
    class="bg-[#12181b] border border-gray-800 rounded-2xl p-6 text-center flex flex-col hover:border-[#00E5A3] transition-colors h-full"
  >
    <div class="text-3xl mb-3">📜</div>
    <h3 class="text-base font-bold mb-2 leading-snug">
      {{ title }}
    </h3>
    <p class="text-gray-400 text-xs leading-relaxed flex-1">
      {{ desc }}
    </p>
  </div>
</template>