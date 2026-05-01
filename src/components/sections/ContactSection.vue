<template>
  <section id="contact" class="w-full bg-[#111111] py-12 px-6 sm:px-12 lg:px-24 text-white">
    <div class="max-w-6xl mx-auto flex flex-col pt-12 items-center">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-4">
          Get In <span class="text-[#00df9a]">Touch</span>
        </h2>
        <div class="h-1 w-32 bg-linear-to-r from-[#00df9a] to-blue-500 mx-auto mb-6"></div>
        <p class="text-gray-400 text-sm md:text-base">
          I'm open to collaboration, projects, or opportunities. Feel free to reach out!
        </p>
      </div>

      <div class="w-full grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-10 mb-16 px-4">
        <div class="flex flex-col">
          <h3 class="text-2xl font-bold mb-4">Let's Connect</h3>
          <p class="text-gray-400 mb-10 text-sm leading-relaxed">
            I'm always open to discussing new projects, creative ideas, or opportunities to be part
            of your vision.
          </p>

          <div class="flex flex-col gap-6">
            <div class="flex items-start gap-4">
              <div class="mt-1 text-2xl text-[#00df9a] w-8 text-center">✉︎</div>
              <div>
                <p class="font-bold text-sm">Email</p>
                <p class="text-gray-400 text-sm">arkanrasendriya@gmail.com</p>
              </div>
            </div>

            <div class="flex items-start gap-4">
              <div class="mt-1 text-2xl text-[#00df9a] w-8 text-center">ℹ️</div>
              <div>
                <p class="font-bold text-sm">LinkedIn</p>
                <a
                  href="https://www.linkedin.com/in/falih-arkan/"
                  target="_blank"
                  class="text-gray-400 hover:text-white transition-colors text-sm"
                  >https://www.linkedin.com/in/falih-arkan/</a
                >
              </div>
            </div>

            <div class="flex items-start gap-4">
              <div class="mt-1 text-2xl text-[#00df9a] w-8 text-center">💻</div>
              <div>
                <p class="font-bold text-sm">GitHub</p>
                <a
                  href="https://github.com/FArkan-15"
                  target="_blank"
                  class="text-gray-400 hover:text-white transition-colors text-sm"
                  >https://github.com/FArkan-15</a
                >
              </div>
            </div>

            <div class="flex items-start gap-4">
              <div class="mt-1 text-2xl text-[#00df9a] w-8 text-center">📍</div>
              <div>
                <p class="font-bold text-sm">Location</p>
                <p class="text-gray-400 text-sm">Sleman, Yogyakarta, Indonesia</p>
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-col justify-center items-center gap-4">
          <img
            src="@/assets/contact-illustration.png"
            alt="Contact illustration"
            class="w-full max-w-md object-contain opacity-80"
          />
        </div>
      </div>
    </div>
  </section>
</template>
