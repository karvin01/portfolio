<template>
  <main class="relative z-10 max-w-[1280px] mx-auto grid grid-cols-4 md:grid-cols-12 gap-x-8 gap-y-12 px-6 py-20 min-h-screen items-center">

    <section class="col-span-4 md:col-span-7 flex flex-col justify-center text-center md:text-left">
      <h1 class="text-5xl md:text-7xl font-black uppercase tracking-tighter"
          style="color: var(--color-main); filter: drop-shadow(0 0 20px rgba(6, 182, 212, 0.4));">
        Karel Vinický
      </h1>
      <p class="mt-6 text-xl md:text-2xl text-cyan-300 font-mono tracking-widest uppercase">
        // Frontend Web Developer
      </p>
      <p class="mt-8 text-gray-400 font-mono text-base md:text-lg max-w-2xl mx-auto md:mx-0">
        Transforming static visions into interactive realities. Specialized in building modern web applications with a focus on clean code and great user experience.
      </p>
    </section>

    <aside class="col-span-4 md:col-span-5 flex justify-center items-center">
      <div class="relative group">
        <div class="absolute -inset-1 bg-main rounded-full opacity-25 blur-xl group-hover:opacity-40 transition-opacity"></div>
        <img
          src="/src/assets/images/CV_profilepic_final.jpg"
          alt="Karel Vinický"
          class="relative w-72 h-72 md:w-96 md:h-96 rounded-full object-cover border-4 border-zinc-800 shadow-2xl"
        />
      </div>
    </aside>

    <nav class="col-span-full mt-16 w-full flex justify-center md:justify-start">
      <div class="flex flex-wrap justify-center md:justify-start gap-8 md:gap-12 w-full">
        <a href="#about" class="button-cyber">
          <span class="relative z-20">About_me</span>
        </a>
        <a href="#projects" class="button-cyber">
          <span class="relative z-20">Projects</span>
        </a>
        <a href="#contact" class="button-cyber">
          <span class="relative z-20">Contact_me</span>
        </a>
      </div>
    </nav>
  </main>
</template>

<script setup>
// Tady zatím nepotřebuješ žádnou logiku, jen čisté HTML/CSS
</script>
