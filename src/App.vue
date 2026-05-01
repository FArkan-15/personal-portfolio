<script setup>
import Navbar from './components/layout/Navbar.vue'
import AboutSection from './components/sections/AboutSection.vue'
import HeroSection from './components/sections/HeroSection.vue'
import ProjectSection from './components/sections/ProjectSection.vue'
import SkillsSection from './components/sections/SkillsSection.vue'
import CertificationSection from './components/sections/CertificationSection.vue'
import AwardSection from './components/sections/AwardSection.vue'
import ContactSection from './components/sections/ContactSection.vue'
import Footer from './components/layout/Footer.vue'

</script>

<template>
  <div class="relative">
    <Navbar />
    <div class="overflow-x-hidden">
      <HeroSection />
      <AboutSection />
      <ProjectSection />
      <SkillsSection />
      <CertificationSection />
      <AwardSection />
      <ContactSection />
      <Footer />
    </div>
  </div>
</template>

<style scoped></style>
