<template>
  <footer class="bg-black border-t border-green-500/20 py-4 px-6">
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-center">
        <!-- Copyright -->
        <div class="text-gray-400 mb-4 md:mb-0">
          © {{ currentYear }} Mon Portfolio. Tous droits réservés.
        </div>
        
        <!-- Logo -->
        <div class="text-green-400 font-bold text-2xl mb-4 md:mb-0">
          <span class="text-white">Port</span>folio
        </div>
        
       
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>