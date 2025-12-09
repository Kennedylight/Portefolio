<template>
  <section id="home" class="pt-32 pb-10 px-6 min-h-screen flex items-center">
    <div class="container mx-auto">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <!-- Texte -->
        <div>
          <h1 class="text-5xl md:text-7xl font-bold mb-6">
            <span class="text-green-400 block">Développeur Full-Stack & Mobile</span>
          </h1>
          <p class="text-gray-400 text-lg mb-8 max-w-lg">
          Développeur Full-Stack & Mobile passionné, je crée des applications web et mobiles modernes, performantes et intuitives. Toujours curieux, je transforme
           les idées en projets concrets et impactants. </p>
          <div class="flex space-x-4">
            <a href="#projects" class="bg-green-500 text-black font-semibold px-8 py-3 rounded-lg hover:bg-green-600">
              Voir mes projets
            </a>
            <a href="#contact" class="border border-green-500 text-green-400 font-semibold px-8 py-3 rounded-lg hover:bg-green-500/10 ">
              Me contacter
            </a>
          </div>
        </div>
        
        <!-- Illustration/Image -->
        <div class="relative">
          <div class="w-full h-96  from-green-500/20 to-black rounded-2xl border border-green-500/30 flex items-center justify-center">
           <img src="/12.png" class="w-full h-hull object-cover rounde-md" alt="">
          </div>
          <div class="absolute -inset-4 border border-green-500/20 rounded-2xl -z-10"></div>
        </div>
      </div>
    </div>
  </section>
</template>