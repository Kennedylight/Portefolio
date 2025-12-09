<template>
  <section id="contact" class="py-20 px-6">
    <div class="container mx-auto max-w-4xl">
      <h2 class="text-4xl font-bold mb-12 text-center">
        <span class="text-white">Me</span>
        <span class="text-green-400"> contacter</span>
      </h2>
      
      <div class="grid md:grid-cols-2 gap-12">
        <!-- Formulaire -->
        <div class="bg-black/50 p-8 rounded-xl border border-green-500/20">
          <form @submit.prevent="submitForm" class="space-y-6">
            <div>
              <label class="block text-gray-300 mb-2">Nom</label>
              <input type="text" v-model="form.name"
                     class="w-full px-4 py-3 bg-gray-900 border border-gray-700 rounded-lg focus:border-green-500 focus:ring-2 focus:ring-green-500/20 outline-none transition-all">
            </div>
            
            <div>
              <label class="block text-gray-300 mb-2">Email</label>
              <input type="email" v-model="form.email"
                     class="w-full px-4 py-3 bg-gray-900 border border-gray-700 rounded-lg focus:border-green-500 focus:ring-2 focus:ring-green-500/20 outline-none transition-all">
            </div>
            
            <div>
              <label class="block text-gray-300 mb-2">Message</label>
              <textarea v-model="form.message" rows="5"
                        class="w-full px-4 py-3 bg-gray-900 border border-gray-700 rounded-lg focus:border-green-500 focus:ring-2 focus:ring-green-500/20 outline-none transition-all resize-none"></textarea>
            </div>
            
            <button type="submit"
                    class="w-full bg-green-500 text-black font-bold py-3 rounded-lg hover:bg-green-600 transition-colors">
              Envoyer le message
            </button>
          </form>
        </div>
        
        <!-- Informations -->
        <div class="space-y-8">
          <div>
            <h3 class="text-2xl font-bold mb-4 text-green-400">Restons en contact</h3>
            <p class="text-gray-400">
              Vous avez un projet en tête ? N'hésitez pas à me contacter. Je réponds généralement dans les 24 heures.
            </p>
          </div>
          
          <div class="space-y-4">
            <div v-for="contact in contactInfo" :key="contact.type"
                 class="flex items-center space-x-4 p-4 bg-black/30 rounded-lg border border-green-500/10">
                 <div class="text-xl" v-html="contact.icon"></div>
              
              <div>
                <p class="text-gray-400 text-sm">{{ contact.type }}</p>
                <p class="text-white">{{ contact.value }}</p>
              </div>
            </div>
          </div>
          
          <!-- Réseaux sociaux -->
          <div>
            <h4 class="text-lg font-semibold mb-4 text-gray-300">Suivez-moi</h4>
            <div class="flex space-x-4">
              <a v-for="social in socialLinks" :key="social.name"
                 :href="social.link" _blank
                 class="w-12 h-12 flex items-center justify-center bg-white/50 border border-green-500/20 rounded-lg text-green-400 hover:bg-white/80 transition-colors">
                <img :src="'/'+social.icon" class="contain w-6 h-6"  alt="">
                 
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
      form: {
        name: '',
        email: '',
        message: ''
      },
      contactInfo: [
        { type: 'Email', value: 'kennedylight05@gmail.com', icon: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
</svg>
` },
        { type: 'Téléphone', value: '+237 689414205', icon: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z" />
</svg>
` },
        { type: 'Localisation', value: 'Douala, Cameroun', icon: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
  <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z" />
</svg>
` }
      ],
      socialLinks: [
        { name: 'GitHub', icon: 'github.png', link: 'https://github.com/Kennedylight' },
        { name: 'LinkedIn', icon: 'linkedin.png', link: 'https://www.linkedin.com/in/kouonga-kennedy-9832a6396?utm_source=share_via&utm_content=profile&utm_medium=member_android' },
        { name: 'Twitter', icon: 'twitter.png', link: '#' }
      ]
    }
  },
  methods: {
    submitForm() {
      // Ici vous ajouterez la logique d'envoi du formulaire
      console.log('Formulaire envoyé:', this.form);
      alert('Message envoyé! (Fonctionnalité à implémenter)');
      this.form = { name: '', email: '', message: '' };
    }
  }
}
</script>