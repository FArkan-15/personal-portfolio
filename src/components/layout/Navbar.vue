<script setup>
import { onMounted, onUnmounted, ref } from 'vue'

const menuOpen = ref(false)
const activeSection = ref('home')
const NAV_OFFSET_PX = 96

const linkBaseClass = 'cursor-pointer px-3 py-1 rounded-md font-medium transition duration-200'
const linkInactiveClass = 'text-[#A3A3A3] hover:text-white hover:bg-gray-800'
const linkActiveClass = 'text-[#00E5A3] bg-[#00E5A3]/10'

const getLinkClass = (sectionId) =>
  `${linkBaseClass} ${activeSection.value === sectionId ? linkActiveClass : linkInactiveClass}`

const setActive = (sectionId) => {
  activeSection.value = sectionId
}
const handleResize = () => {
  if (window.innerWidth >= 768) {
    menuOpen.value = false
  }
}

onMounted(() => {
  window.addEventListener('resize', handleResize)

  const sectionIds = ['home', 'about', 'projects', 'skills', 'certifications', 'awards', 'contact']

  let isTicking = false

  const updateActiveByScroll = () => {
    const scrollPos = window.scrollY + NAV_OFFSET_PX + 1
    let current = 'home'

    for (const id of sectionIds) {
      const el = document.getElementById(id)
      if (!el) continue
      const top = el.offsetTop
      if (top <= scrollPos) current = id
    }

    activeSection.value = current
  }

  const onScroll = () => {
    if (isTicking) return
    isTicking = true
    window.requestAnimationFrame(() => {
      updateActiveByScroll()
      isTicking = false
    })
  }

  window.addEventListener('scroll', onScroll, { passive: true })
  updateActiveByScroll()

  onUnmounted(() => {
    window.removeEventListener('scroll', onScroll)
  })
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
            <a href="#home" :class="getLinkClass('home')" @click="setActive('home')">Home</a>
          </li>
          <li>
            <a href="#about" :class="getLinkClass('about')" @click="setActive('about')">About</a>
          </li>
          <li>
            <a href="#projects" :class="getLinkClass('projects')" @click="setActive('projects')"
              >Projects</a
            >
          </li>
          <li>
            <a href="#skills" :class="getLinkClass('skills')" @click="setActive('skills')"
              >Skills</a
            >
          </li>
          <li>
            <a
              href="#certifications"
              :class="getLinkClass('certifications')"
              @click="setActive('certifications')"
              >Certifications</a
            >
          </li>
          <li>
            <a href="#awards" :class="getLinkClass('awards')" @click="setActive('awards')"
              >Awards</a
            >
          </li>
          <li>
            <a href="#contact" :class="getLinkClass('contact')" @click="setActive('contact')"
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
          @click="
            menuOpen = false
            setActive('home')
          "
          href="#home"
          :class="getLinkClass('home')"
          >Home</a
        >
        <a
          @click="
            menuOpen = false
            setActive('about')
          "
          href="#about"
          :class="getLinkClass('about')"
          >About</a
        >
        <a
          @click="
            menuOpen = false
            setActive('projects')
          "
          href="#projects"
          :class="getLinkClass('projects')"
          >Projects</a
        >
        <a
          @click="
            menuOpen = false
            setActive('skills')
          "
          href="#skills"
          :class="getLinkClass('skills')"
          >Skills</a
        >
        <a
          @click="
            menuOpen = false
            setActive('certifications')
          "
          href="#certifications"
          :class="getLinkClass('certifications')"
          >Certifications</a
        >
        <a
          @click="
            menuOpen = false
            setActive('awards')
          "
          href="#awards"
          :class="getLinkClass('awards')"
          >Awards</a
        >
        <a
          @click="
            menuOpen = false
            setActive('contact')
          "
          href="#contact"
          :class="getLinkClass('contact')"
          >Contact</a
        >
      </div>
    </div>
  </nav>
</template>
