<template>
  <section id="projects" class="relative z-20 bg-zinc-900 w-full pb-32 scroll-mt-20">
    <div class="max-w-[1280px] mx-auto px-6 grid grid-cols-4 md:grid-cols-12 gap-y-10">

      <SectionHeader title="Projects" />

      <div
        v-for="project in projects"
        :key="project.id"
        class="col-span-4 md:col-span-12 group relative"
      >
        <div class="absolute -inset-1 bg-main/20 opacity-0 group-hover:opacity-100 transition-opacity duration-500 z-0"
             style="clip-path: polygon(40px 0, 100% 0, 100% calc(100% - 40px), calc(100% - 40px) 100%, 0 100%, 0 40px);"></div>

        <div class="relative z-10 bg-zinc-950 border border-zinc-800 p-6 md:p-10 flex flex-col md:flex-row gap-10 items-center"
             style="clip-path: polygon(40px 0, 100% 0, 100% calc(100% - 40px), calc(100% - 40px) 100%, 0 100%, 0 40px);">

          <div class="w-full md:w-3/5 aspect-video bg-zinc-900 border border-zinc-800 overflow-hidden relative">
            <img
              :src="project.img"
              :alt="project.title"
              class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700"
            />
            <div class="absolute inset-0 bg-main/5 mix-blend-overlay"></div>
          </div>

          <div class="w-full md:w-2/5 space-y-6 text-left">
            <div>
              <div class="text-main font-mono text-xs mb-2 tracking-tighter">{{ project.tag }}</div>
              <h3 class="text-3xl font-black text-white uppercase tracking-tighter italic">
                {{ project.title }}
              </h3>
            </div>

            <p class="text-gray-400 font-mono text-sm leading-relaxed">
              {{ project.desc }}
            </p>

            <div class="flex flex-wrap gap-2 pt-2">
              <span
                v-for="tech in project.tech"
                :key="tech"
                class="font-mono text-xs text-main bg-main/5 px-4 h-7 flex items-center border border-main/40 uppercase tracking-wider"
              >
                {{ tech }}
              </span>
            </div>

            <div class="pt-4">
              <a href="#"
                 class="inline-block relative bg-main text-zinc-950 px-8 py-3 font-black uppercase text-xs tracking-[0.2em] hover:bg-white transition-colors duration-300"
                 style="clip-path: polygon(10px 0, 100% 0, 100% calc(100% - 10px), calc(100% - 10px) 100%, 0 100%, 0 10px);">
                View_Case_Study
              </a>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    id: 1,
    tag: "01 // FE_DEVELOPMENT",
    title: "Project_Alpha",
    desc: "Custom dashboard design with real-time data visualization. Focusing on clean UI and brutalist aesthetics.",
    tech: ["VUE_JS", "TAILWIND", "VITE"],
    img: "https://picsum.photos/id/10/1200/800"
  },
  {
    id: 2,
    tag: "02 // WEB_DESIGN",
    title: "Cyber_Portfolio",
    desc: "Interactive portfolio with Matrix rain background and custom video integration. Optimized for performance.",
    tech: ["VUE_JS", "GSAP", "CSS_GRID"],
    img: "https://picsum.photos/id/20/1200/800"
  },
  {
    id: 3,
    tag: "03 // UI_UX",
    title: "Neural_Interface",
    desc: "A futuristic interface for data management systems with focus on accessibility and motion design.",
    tech: ["FIGMA", "VUE_JS", "TAILWIND"],
    img: "https://picsum.photos/id/30/1200/800"
  },
  {
    id: 4,
    tag: "04 // BACKEND",
    title: "Data_Core",
    desc: "Robust API structure for managing large datasets with real-time updates and secure authentication.",
    tech: ["NODE_JS", "POSTGRES", "DOCKER"],
    img: "https://picsum.photos/id/40/1200/800"
  },
  {
    id: 5,
    tag: "05 // EXPERIMENTAL",
    title: "Void_Runner",
    desc: "Web-based game engine experiment using Three.js and custom shaders for high-end visuals.",
    tech: ["THREE_JS", "WEBGL", "JS_CANVAS"],
    img: "https://picsum.photos/id/50/1200/800"
  }
];
import SectionHeader from './SectionHeader.vue';
</script>
