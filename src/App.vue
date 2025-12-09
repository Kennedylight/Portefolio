<template>
  <div id="app" class="w-full bg-black text-gray-100">
    <Header />
    <main>
      <Hero />
      <About />
      <Langages />
      <Projects />
      <Skills />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Langages from './components/Langages.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    About,
    Langages,
    Projects,    
    Contact,
    Footer
  }
}
</script>