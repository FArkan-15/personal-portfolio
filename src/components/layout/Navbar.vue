<script setup>
import { onMounted, onUnmounted, ref } from 'vue'

const menuOpen = ref(false)
const handleResize = () => {
  if (window.innerWidth >= 768) {
    menuOpen.value = false
  }
}

onMounted(() => {
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})
</script>

<template>
  <nav
    class="bg-[#0A0A0A] w-full px-6 py-4 backdrop-blur-md border-b border-gray-800 sticky top-0 z-50"
  >
    <div class="flex justify-between items-center max-w-6xl mx-auto">
      <div class="text-white font-bold text-xl relative z-50">
        <h1>Portfolio</h1>
      </div>
      <div class="flex-1 flex justify-end">
        <ul class="hidden md:flex gap-1">
          <li>
            <a
              href="#home"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Home</a
            >
          </li>
          <li>
            <a
              href="#about"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >About</a
            >
          </li>
          <li>
            <a
              href="#projects"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Projects</a
            >
          </li>
          <li>
            <a
              href="#skills"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Skills</a
            >
          </li>
          <li>
            <a
              href="#certifications"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Certifications</a
            >
          </li>
          <li>
            <a
              href="#awards"
              class="text-[#A3A3A3] hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Awards</a
            >
          </li>
          <li>
            <a
              href="#contact"
              class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
              >Contact</a
            >
          </li>
        </ul>
      </div>
      <div class="relative z-50">
        <button
          class="md:hidden text-white flex flex-col justify-between h-5 w-6 relative z-50"
          @click="menuOpen = !menuOpen"
        >
          <div
            class="absolute w-6 h-0.5 bg-white rounded-full transform transition-all duration-300 left-0"
            :class="menuOpen ? 'rotate-45 top-2.5' : 'top-0'"
          ></div>
          <div
            class="absolute w-6 h-0.5 bg-white rounded-full transition-all duration-300 left-0 top-2.5"
            :class="menuOpen ? 'opacity-0' : 'opacity-100'"
          ></div>
          <div
            class="absolute w-6 h-0.5 bg-white rounded-full transform transition-all duration-300 left-0"
            :class="menuOpen ? '-rotate-45 top-2.5' : 'top-5'"
          ></div>
        </button>
      </div>
    </div>
    <div
      class="md:hidden fixed top-0 right-0 w-72 h-screen bg-[#0A0A0A] border-l border-gray-800 z-50 transform transition duration-300"
      :class="
        menuOpen ? 'translate-x-0 pointer-events-auto' : 'translate-x-full pointer-events-none'
      "
    >
      <div class="flex flex-col gap-1 mt-24 px-8 text-xl overflow-hidden relative z-50">
        <a
          @click="menuOpen = false"
          href="#home"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Home</a
        >
        <a
          @click="menuOpen = false"
          href="#about"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >About</a
        >
        <a
          @click="menuOpen = false"
          href="#projects"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Projects</a
        >
        <a
          @click="menuOpen = false"
          href="#skills"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Skills</a
        >
        <a
          @click="menuOpen = false"
          href="#certifications"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Certifications</a
        >
        <a
          @click="menuOpen = false"
          href="#awards"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Awards</a
        >
        <a
          @click="menuOpen = false"
          href="#contact"
          class="text-gray-400 hover:text-white cursor-pointer hover:bg-gray-800 px-3 py-1 rounded-md font-medium transition duration-200"
          >Contact</a
        >
      </div>
    </div>
  </nav>
</template>
