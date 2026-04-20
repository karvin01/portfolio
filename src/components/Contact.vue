<template>
  <section id="contact" class="relative z-20 bg-zinc-900 w-full pb-32 scroll-mt-20">
    <div class="max-w-[1280px] mx-auto px-6 grid grid-cols-4 md:grid-cols-12 gap-y-12">

      <SectionHeader title="Contact_me" class="md:col-start-3 md:col-span-8"/>

      <div class="col-span-4 md:col-start-2 md:col-span-10 lg:col-start-3 lg:col-span-8">
        <form @submit.prevent="handleSubmit" class="space-y-8 font-mono">

          <div class="group">
            <label class="block text-main text-xs uppercase mb-3 ml-1 tracking-widest">// Full_Name</label>
            <input
              type="text"
              placeholder="Your Name"
              class="w-full bg-zinc-950 border border-zinc-800 p-4 text-white outline-none focus:border-main/60 transition-all duration-300"
              style="clip-path: polygon(0 0, 100% 0, 100% 70%, calc(100% - 15px) 100%, 0 100%);"
            />
          </div>

          <div class="group">
            <label class="block text-main text-xs uppercase mb-3 ml-1 tracking-widest">// Email_Address</label>
            <input
              type="email"
              placeholder="your@email.com"
              class="w-full bg-zinc-950 border border-zinc-800 p-4 text-white outline-none focus:border-main/60 transition-all duration-300"
              style="clip-path: polygon(0 0, 100% 0, 100% 70%, calc(100% - 15px) 100%, 0 100%);"
            />
          </div>

          <div class="group">
            <label class="block text-main text-xs uppercase mb-3 ml-1 tracking-widest">// Message_Content</label>
            <textarea
              rows="5"
              placeholder="System message..."
              class="w-full bg-zinc-950 border border-zinc-800 p-4 text-white outline-none focus:border-main/60 transition-all duration-300 resize-none"
              style="clip-path: polygon(0 0, 100% 0, 100% 85%, calc(100% - 25px) 100%, 0 100%);"
            ></textarea>
          </div>

          <div class="pt-4">
            <button
              type="submit"
              class="bg-main text-zinc-950 px-12 py-4 font-black uppercase text-xs tracking-[0.3em] hover:bg-white transition-all duration-300 shadow-[0_0_20px_rgba(6,182,212,0.3)]"
              style="clip-path: polygon(15px 0, 100% 0, 100% calc(100% - 15px), calc(100% - 15px) 100%, 0 100%, 0 15px);"
            >
              Send
            </button>
          </div>
        </form>

        <div class="mt-24 pt-12 border-t border-zinc-800 flex flex-col md:flex-row justify-between items-start md:items-center gap-10 font-mono">

          <div class="space-y-4">
            <div class="flex items-center gap-4 text-zinc-400 group">
              <svg viewBox="0 0 24 24" class="w-5 h-5 fill-main/70 group-hover:fill-main transition-colors"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
              <a href="mailto:karelvi@centrum.cz" class="hover:text-main transition-colors">karelvi@centrum.cz</a>
            </div>
            <div class="flex items-center gap-4 text-zinc-400">
              <svg viewBox="0 0 24 24" class="w-5 h-5 fill-main/70"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
              <span>+420 733 544 788</span>
            </div>
          </div>

          <div class="flex gap-8 items-center">
            <a href="https://www.linkedin.com/in/karel-vinicky/" target="_blank" class="text-zinc-500 hover:text-main hover:-translate-y-1 transition-all duration-300">
              <svg viewBox="0 0 24 24" style="width: 28px; height: 28px;" class="fill-current">
                <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/>
              </svg>
            </a>

            <a href="https://github.com/karvin01" target="_blank" class="text-zinc-500 hover:text-main hover:-translate-y-1 transition-all duration-300">
              <svg viewBox="0 0 24 24" style="width: 24px; height: 24px;" class="fill-current">
                <path d="M12 .3a12.1 12.1 0 0 0-3.8 23.4c.6.1.8-.3.8-.6v-2.2c-3.3.7-4-1.4-4-1.4-.6-1.4-1.4-1.8-1.4-1.8-1.1-.7.1-.7.1-.7 1.2.1 1.9 1.2 1.9 1.2 1.1 1.8 2.8 1.3 3.5 1 .1-.8.4-1.3.8-1.6-2.7-.3-5.5-1.3-5.5-5.9 0-1.3.5-2.4 1.3-3.2-.1-.3-.5-1.5.1-3.2 0 0 1-.3 3.3 1.2a11.5 11.5 0 0 1 6 0c2.3-1.5 3.3-1.2 3.3-1.2.6 1.7.2 2.9.1 3.2.8.8 1.3 1.9 1.3 3.2 0 4.6-2.8 5.6-5.5 5.9.4.4.8 1.1.8 2.2v3.3c0 .3.2.7.8.6A12.1 12.1 0 0 0 12 .3"/>
              </svg>
            </a>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import SectionHeader from './SectionHeader.vue';

const handleSubmit = () => {
  // Jen vizuální feedback pro test
  console.log("Form submitted locally.");
};
</script>
