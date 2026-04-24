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
              <a :href="project.link"
                  target="_blank"
                 class="inline-block relative bg-main text-zinc-950 px-8 py-3 font-black uppercase text-xs tracking-[0.2em] hover:bg-white transition-colors duration-300"
                 style="clip-path: polygon(10px 0, 100% 0, 100% calc(100% - 10px), calc(100% - 10px) 100%, 0 100%, 0 10px);">
                 {{ project.linkText }}
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
    desc: "Every expert was once a beginner, and this was my start. Working with just HTML and CSS, I built this project and discovered a genuine love for web development. It’s a reminder of where I began and the spark that keeps me coding today.",
    tech: ["HTML", "CSS"],
    img: "/src/assets/images/Recipe-page.jpeg",
    link: "https://github.com/karvin01/recipe-page-mandatory",
    linkText: "View_Github"
  },
  {
    id: 2,
    tag: "02 // FE_DEVELOPMENT",
    title: "Brothers_Lionheart",
    desc: "I developed the project’s frontend foundation, building a home page with reusable CSS patterns that served as a template for the entire team. I also implemented the responsive design, ensuring a seamless experience across mobile, tablet, and desktop devices.",
    tech: ["HTML", "CSS"],
    img: "/src/assets/images/Brothers-lionheart.jpeg",
    link: "https://github.com/karvin01/Semester-project-webpage",
    linkText: "View_Github"
  },
  {
    id: 3,
    tag: "03 // UI_UX",
    title: "CO2_saving_app",
    desc: "I collaborated on the UX/UI strategy for a green lifestyle app that gamifies sustainability through daily challenges. I focused on creating an intuitive user journey and a clean interface that motivates users to build eco-friendly habits. My work ensured the design was both visually engaging and logically structured to encourage daily engagement.",
    tech: ["FIGMA"],
    img: "/src/assets/images/UX-CO2-app.jpg",
    link: "https://www.figma.com/design/flLyxAIjjM2iRei4FaaZsl/UX-CO2-app?node-id=0-1&t=e4ld0Z6m4sOXCx4N-0",
    linkText: "View_Figma"
  },
  {
    id: 4,
    tag: "04 // INDESIGN",
    title: "Business_card",
    desc: "I designed a custom business card featuring a minimalistic logo based on my initials. The goal was to establish a strong personal brand by maintaining visual coherency with my portfolio’s aesthetic. This project allowed me to focus on typography, layout, and the power of a 'less is more' design philosophy.",
    tech: ["INDESIGN", "ILLUSTRATOR"],
    img: "/src/assets/images/businesscard.jpg",
    link: "/src/assets/pdf/Business_card.pdf",
    linkText: "View_PDF"
  },
  {
    id: 5,
    tag: "05 // DEVELOPMENT",
    title: "Portfolio_from_scratch",
    desc: "This is my most advanced project to date and the first I’ve built entirely from scratch. It started as a custom design in Figma, which I then built out, using AI to help refine the code while I made sure the design stayed exactly how I wanted it. My goal was to capture a \"nerdy\" yet professional vibe that truly represents me as a frontend developer.",
    tech: ["VUE_JS", "HTML", "TAILWIND", "FIGMA"],
    img: "/src/assets/images/portfolio_website.jpeg",
    link: "https://github.com/karvin01/portfolio",
    linkText: "View_Github"
  }
];
import SectionHeader from './SectionHeader.vue';
</script>
