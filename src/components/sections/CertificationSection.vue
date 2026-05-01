<script setup>
import CertificationCard from './CertificationCard.vue'
</script>

<template>
  <section id="certifications" class="bg-[#111111] text-white py-20 px-6">
    <div class="max-w-5xl mx-auto">
      <div class="text-center mb-12 flex flex-col items-center">
        <h2 class="text-4xl font-bold font-sans">Certifications</h2>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5">
        
        <CertificationCard
          title="AI Training – Collective Partner Batch 2"
          desc="Introductory training on artificial intelligence concepts and applications. Generation Girls · 2025"
        />

        <CertificationCard
          title="IT-CAS Competition – UI/UX Web Design"
          desc="Participant – IT-CAS Competition (UI/UX Web Design). STMIK AMIKOM Surakarta · 2025"
        />

        <CertificationCard
          title="Fundamentals of Artificial Intelligence"
          desc="Learned basic AI concepts including machine learning fundamentals. Dicoding Indonesia · 2025"
        />

        <CertificationCard
          title="Python Programming Bootcamp"
          desc="Learned Python basics including syntax and logic. Special Skill Indonesia · 2025"
        />

        <CertificationCard
          title="RevoU Coding Camp – Intro to Software Engineering"
          desc="Introduction to software engineering concepts. RevoU · 2025"
        />

        <CertificationCard
          title="UPY Mathematics Competition (National Level)"
          desc="Participant in a national-level mathematics competition. UPY · 2026"
        />

      </div>
    </div>
  </section>
</template>
