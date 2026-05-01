<template>
  <section id="about" class="bg-[#0a0a0a] text-white py-20 px-6">
    <div class="max-w-6xl mx-auto">
      <div class="mb-12">
        <h2 class="text-4xl font-bold mb-2">About <span class="text-[#00E5A3]">Me</span></h2>
        <div class="w-16 h-1 bg-[#00E5A3] mt-2 rounded"></div>
      </div>

      <div class="flex flex-col lg:flex-row gap-12 items-start">
        <div class="w-full lg:w-1/3 shrink-0">
          <img
            src="@/assets/profile-falih-arkan.jpeg"
            alt="Falih Arkan"
            class="w-full h-auto rounded-3xl object-cover border-2 border-transparent bg-gray-800 min-h-[500px]"
          />
        </div>

        <div class="w-full lg:w-2/3 flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold mb-1">Falih Arkan Al Fathani Rasendriya</h3>
            <p class="text-gray-400 text-sm mb-6">
              Student of Information Systems, Networking & Applications
            </p>

            <div class="text-gray-300 space-y-4 text-sm leading-relaxed mb-10">
              <p>
                I am a vocational high school student majoring in Information Systems, Networking,
                and Applications, with hands-on experience in web development, UI/UX design, and
                basic server administration.
              </p>
              <p>
                I have worked on various school and personal projects, including building static
                websites using HTML, CSS, and JavaScript, developing company portfolio websites, and
                setting up a Proxmox-based homelab to deploy and manage a Minecraft server.
              </p>
              <p>
                I have also participated in national-level competitions and technology events,
                earning Bronze Medals in informatics and mathematics olympiads. I am highly
                motivated to continue learning and improving my skills in technology, design, and
                system development. Let's build something amazing together!
              </p>
            </div>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
            <div
              class="bg-[#0f1619] border border-green-800 rounded-xl p-5 hover:border-[#00E5A3] transition-colors"
            >
              <div class="text-2xl mb-3">💻</div>
              <h4 class="font-bold text-sm mb-2">Web Development</h4>
              <p class="text-gray-400 text-xs">HTML, CSS, JavaScript, responsive websites</p>
            </div>

            <div
              class="bg-[#0f1619] border border-green-800 rounded-xl p-5 hover:border-[#00E5A3] transition-colors"
            >
              <div class="text-2xl mb-3">🎨</div>
              <h4 class="font-bold text-sm mb-2">UI/UX Design</h4>
              <p class="text-gray-400 text-xs">Basic wireframing & interface design</p>
            </div>

            <div
              class="bg-[#0f1619] border border-green-800 rounded-xl p-5 hover:border-[#00E5A3] transition-colors"
            >
              <div class="text-2xl mb-3">🖥️</div>
              <h4 class="font-bold text-sm mb-2">Networking & Server</h4>
              <p class="text-gray-400 text-xs">Proxmox, basic server & homelab setup</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
