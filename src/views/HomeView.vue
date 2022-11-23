<template>
  <div>
    <Navbar />
    <Contenuhomepage />
    <Nosplats />
    <Nosextras />
    <Promotion />
    <Avis />
    <Astuce />
    <Contacteznous />
    <Avantages />
    <Footer />
    <Blog />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/homepage/Navbar.vue'
import Contenuhomepage from '@/components/homepage/Contenuhomepage.vue'
import Nosplats from '@/components/nosoffres/Nosplats.vue'
import Nosextras from '@/components/nosoffres/Nosextras.vue'
import Promotion from '@/components/promotion/Promotion.vue'
import Avis from '@/components/Avis.vue'
import Astuce from '@/components/Astuce.vue'
import Contacteznous from '@/components/Contacteznous.vue'
import Avantages from '@/components/Avantages.vue'
import Footer from '@/components/Footer.vue'
import Blog from '@/components/Blog.vue'

export default {
  name: 'HomeView',
  components: {
    Navbar,
    Contenuhomepage,
    Nosplats, 
    Nosextras,
    Promotion,
    Avis,
    Astuce,
    Contacteznous,
    Avantages,
    Footer,
    Blog
  }
}
</script>
