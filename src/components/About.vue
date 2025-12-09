<template>
  <section id="about" class="py-20 px-6 bg-gray-900/50">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold mb-12 text-center">
        <span class="text-white">À propos de</span>
        <span class="text-green-400"> moi</span>
      </h2>
      
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div>
          <p class="text-gray-300 mb-6 text-lg">
           Je suis KOUONGA TADIE KENNEDY, un développeur Full-Stack & Mobile passionné, toujours en quête de nouvelles technologies et de défis à relever. J’aime créer des applications web et mobiles modernes, performantes et intuitives, qui offrent une expérience utilisateur fluide et captivante. Curieux et ambitieux, je transforme les idées en projets concrets, alliant design, logique et innovation pour délivrer des solutions de qualité. Mon objectif : coder intelligemment, créer efficacement et repousser mes limites à chaque projet.
          </p>
          
          <div class="mt-8">
            <a href="/cv.pdf" download class="inline-flex items-center text-green-400 hover:text-green-300">
              <span>Télécharger mon CV</span>
              <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"/>
              </svg>
            </a>
          </div>
        </div>
        
        <div class="grid md:grid-cols-2 grid-cols-1 gap-4">
          <div v-for="item in aboutItems" :key="item.title"
               class="bg-black/50 p-6 rounded-xl border border-green-500/20 hover:border-green-500/40 transition-colors">
            <div class="text-green-400 text-2xl mb-4">{{ item.icon }}</div>
            <h3 class="text-xl font-semibold mb-2">{{ item.title }}</h3>
            <p class="text-gray-400">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      aboutItems: [
  { 
    icon: '🔍', 
    title: 'Curiosité insatiable', 
    description: 'Toujours en quête de nouvelles technologies et méthodes pour améliorer mes projets.' 
  },
  { 
    icon: '⚡', 
    title: 'Polyvalence / Adaptabilité', 
    description: 'Capable de travailler sur le web, le mobile et le backend pour créer des solutions complètes.' 
  },
  { 
    icon: '🎯', 
    title: 'Perfectionnisme orienté qualité', 
    description: 'Je veille à ce que chaque projet soit performant, fluide et agréable pour l’utilisateur.' 
  },
  { 
    icon: '🚀', 
    title: 'Ambition et détermination', 
    description: 'Je relève des défis, transforme les idées en projets concrets et repousse mes limites à chaque fois.' 
  }
]

    }
  }
}
</script>