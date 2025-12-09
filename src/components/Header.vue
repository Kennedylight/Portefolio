<template>
  <header class="fixed w-full bg-black/90 backdrop-blur-sm z-50 border-b-2 border-green-500/20">
    <nav class="container mx-auto px-6 py-4">
      <div class="flex justify-between items-center">
        <!-- Logo -->
        <div class="text-green-400 font-bold text-2xl">
          <span class="text-white">Port</span>folio
        </div>
        
        <!-- Navigation Desktop -->
        <div class="hidden md:flex space-x-8">
          <a v-for="item in navItems" 
             :key="item.name"
             :href="item.href"
             class="text-gray-300 hover:text-green-400  duration-300">
            {{ item.name }}
          </a>
        </div>
        
        <!-- Mobile menu button -->
        <button class="md:hidden text-green-400">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
          </svg>
        </button>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      navItems: [
        { name: 'Accueil', href: '#home' },
        { name: 'À propos', href: '#about' },
        { name: 'Projets', href: '#projects' },
        { name: 'Compétences', href: '#skills' },
        { name: 'Contact', href: '#contact' }
      ]
    }
  }
}
</script>