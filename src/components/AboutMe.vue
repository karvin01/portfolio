<template>
  <div class="relative">
    <div class="h-20 bg-gradient-to-b from-transparent to-zinc-900"></div>

    <section id="about" class="relative z-20 bg-zinc-900 w-full pb-24">
      <div class="max-w-[1280px] mx-auto px-6 grid grid-cols-4 md:grid-cols-12 gap-12 items-start">

        <SectionHeader title="About_me" />

        <div class="col-span-4 md:col-span-6 font-mono leading-relaxed">
          <div class="text-gray-300 space-y-6 text-lg">
            <p>
              My path to frontend development wasn't exactly a straight line. After high school, I started studying economics at Brno University of Technology, but I quickly realized that something was missing. I felt a lack of creativity and missed the satisfaction of actually building something tangible with my own hands.
            </p>
            <p>
              That realization led me to a pretty big decision: I moved to Denmark to study Multimedia Design at SEA Esbjerg. My goal is to follow this up with a Bachelor’s top-up in Web Development.
            </p>
            <p>
              This is where I finally found myself, especially in the coding part of the craft. I’m excited about the future and look forward to building projects that not only look great but also make users genuinely happy with the experience.
            </p>
          </div>

          <div class="mt-10 flex flex-wrap gap-3">
            <span class="text-xs border border-cyan-500/30 px-3 py-1 text-cyan-400 bg-cyan-500/5">SEA_ESBJERG</span>
            <span class="text-xs border border-cyan-500/30 px-3 py-1 text-cyan-400 bg-cyan-500/5">MULTIMEDIA_DESIGN</span>
            <span class="text-xs border border-cyan-500/30 px-3 py-1 text-cyan-400 bg-cyan-500/5">WEB_DEV_TOPUP</span>
          </div>
        </div>

        <div class="col-span-4 md:col-span-6">
          <div class="relative group">
            <div class="absolute -inset-2 border border-cyan-500/10 z-0"></div>

            <div class="relative z-10 aspect-video bg-zinc-950 border border-zinc-800 shadow-2xl overflow-hidden"
                style="clip-path: polygon(0 0, 100% 0, 100% 85%, 85% 100%, 0 100%);">

              <!-- Vysvětlení logiky níže:
              - Pokud video NEHRAJE (!isPlaying), je černobílé (grayscale).
              - Pokud na něj najedeš (group-hover:grayscale-0), zbarví se.
              - Pokud už HRAJE, grayscale se úplně odstraní. -->
              <video
                ref="videoPlayer"
                controls
                class="w-full h-full object-cover transition-all duration-700"
                :class="{ 'grayscale group-hover:grayscale-0': !isPlaying, 'grayscale-0': isPlaying }"
                @play="isPlaying = true"
                @pause="isPlaying = false"
              >
                <source src="/video/cv_video_karel_vinicky.mp4" type="video/mp4">
                Your browser does not support the video tag.
              </video>

              <div
                v-if="!isPlaying"
                class="absolute inset-0 flex items-center justify-center z-30 pointer-events-none transition-opacity duration-300"
                :class="{'opacity-100': !isPlaying, 'opacity-0': isPlaying}"
              >
                <button
                  @click.stop="togglePlay"
                  class="pointer-events-auto w-24 h-24 rounded-full border-4 border-main/70 bg-main grid place-items-center shadow-[0_0_40px_rgba(6,182,212,0.8)] hover:scale-105 transition-all duration-300 group"
                >
                  <!--
                    Text-zinc-950: Barva šipky (tvůj background odstín)
                    Translate-x-1.5: Klíčový optický offset, který šipku posune doprava na optický střed
                  -->
                  <svg
                    viewBox="0 0 24 24"
                    class="w-14 h-14 text-background fill-current"
                  >
                    <path d="M8 5v14l11-7z"/>
                  </svg>
                </button>
              </div>
            </div>

            <div class="mt-4 font-mono text-[10px] text-zinc-500 flex justify-between uppercase tracking-widest">
              <div class="flex items-center gap-2">
                <span class="w-1.5 h-1.5 bg-main animate-pulse rounded-full"></span>
                <span>cv_video_karel_vinicky.mp4</span>
              </div>
              <span class="text-zinc-700">Type: MPEG-4</span>
            </div>
          </div>
        </div>

      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Vytvoříme referenci na video element
const videoPlayer = ref(null);
// Stav, zda video hraje
const isPlaying = ref(false);

// Funkce pro spuštění/pozastavení videa
const togglePlay = () => {
  if (videoPlayer.value.paused) {
    videoPlayer.value.play();
    isPlaying.value = true;
  } else {
    videoPlayer.value.pause();
    isPlaying.value = false;
  }
};

import SectionHeader from './SectionHeader.vue';
</script>
