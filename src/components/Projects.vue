<template>
  <section id="projects" class="py-10 px-6 bg-gray-900/50">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold mb-12 text-center">
        <span class="text-white">Mes</span>
        <span class="text-green-400"> projets</span>
      </h2>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="project in projects" :key="project.title"
             class="bg-black/50 rounded-xl overflow-hidden border border-green-500/20 hover:border-green-500/40 transition-all duration-300 hover:-translate-y-2">
          <!-- Image du projet -->
          <div class="h-48  from-green-900/30  to-black relative overflow-hidden">
            <div class="absolute inset-0 flex items-center justify-center">
             <img :src="'/'+project.icon" class="w-ful h-full object-cover" alt="">
            </div>
          </div>
          
          <!-- Contenu -->
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2">{{ project.title }}</h3>
            <p class="text-gray-400 mb-4">{{ project.description }}</p>
            
            <!-- Technologies -->
            <div class="flex flex-wrap gap-2 mb-4">
              <span v-for="tech in project.technologies" :key="tech"
                    class="px-3 py-1 bg-green-500/10 text-green-400 text-sm rounded-full">
                {{ tech }}
              </span>
            </div>
            
            <!-- Liens -->
            <div class="flex space-x-4">
              <a :href="project.liveLink" _blank class="text-green-400 hover:text-green-300 text-sm font-medium">
                Voir le projet →
              </a>
              <a :href="project.githubLink" _blank class="text-gray-400 hover:text-gray-300 text-sm font-medium">
                Code source
              </a>
            </div>
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
      projects: [
        {
          title: 'Application pour la santé mentale',
          description: 'Site cree avec Vue.js et Tailwind CSS',
          technologies: ['Vue.js', 'Tailwind'],
          icon: 'freeandtalk.png',
          liveLink: 'https://free-talk-l3cm.vercel.app/acceuilcenter',
          githubLink: 'https://github.com/Kennedylight/Free_Talk'
        },
        {
          title: 'CRUD',
          description: 'Crud pour apprendre les bases de react',
          technologies: ['React Native'],
          icon: 'crud.png',
          liveLink: 'https://first-app-react-seven.vercel.app/',
          githubLink: 'https://github.com/Kennedylight/First-app-react'
        },
        
      ]
    }
  }
}
</script>