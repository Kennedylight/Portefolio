<template>
  <section id="skills" class="py-20 px-6 bg-gray-900/50">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold mb-12 text-center">
        <span class="text-white">Mes</span>
        <span class="text-green-400"> compétences</span>
      </h2>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="skill in skills" :key="skill.category"
             class="bg-black/50 p-6 rounded-xl border border-green-500/20">
          <h3 class="text-xl font-bold mb-6 text-green-400">{{ skill.category }}</h3>
          
          <div class="space-y-4">
            <div v-for="item in skill.items" :key="item.name" class="space-y-2">
              <div class="flex justify-between">
                <span class="text-gray-300">{{ item.name }}</span>
                <span class="text-green-400">{{ item.level }}%</span>
              </div>
              <div class="h-2 bg-gray-800 rounded-full overflow-hidden">
                <div class="h-full bg-green-400  from-green-500 to-green-400 rounded-full"
                     :style="{ width: item.level + '%'}" ></div>
              </div>
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
      skills: [
        {
          category: 'Frontend',
          items: [
            { name: 'Vue.js', level: 90 },
            { name: 'JavaScript', level: 85 },
            { name: 'Tailwind CSS', level: 80 },
            { name: 'HTML/CSS', level: 95 },
            { name: 'HTML/CSS', level: 95 }
          ]
        },
        {
          category: 'Outils',
          items: [
            { name: 'Git', level: 85 },
            { name: 'VS Code', level: 90 },
            { name: 'Figma', level: 70 },
            { name: 'Webpack/Vite', level: 75 }
          ]
        },
        {
          category: 'Backend',
          items: [
            { name: 'Node.js', level: 70 },
            { name: 'Firebase', level: 65 },
            { name: 'API REST', level: 80 },
            { name: 'MongoDB', level: 60 }
          ]
        }
      ]
    }
  }
}
</script>