<script>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import Footer from './components/Footer.vue';
import About from './components/About.vue';
import Visit from './components/Visit.vue';
import Collection from './components/Collection.vue';
import Insidecart from './components/Insidecart.vue';
import Sofa from './components/Sofa.vue';
import Contact from './components/Contact.vue';
export default {
  components: {
    Navbar,
    Home,
    Footer,
    About,
    Visit,
    Collection,
    Insidecart,
    Sofa,
    Contact

  },
  data() {
    return {
      currentpage: 'Home',
      cartItems: [],

    }
  },
  methods: {
    changePage(page) {
      this.currentpage = page;
      
    },
    addToMasterCart(sofa) {
      this.cartItems.push({...sofa});
    
    }
  }
}
</script>

<template>
  <Navbar @switchpages="changePage" />
  <Home v-if="currentpage === 'Home'" @addCart="addToMasterCart"/>
  <About v-if="currentpage === 'About'" />
  <Visit v-if="currentpage === 'Visit'" />
  <Collection v-if="currentpage === 'Collect'" />
  <Insidecart v-if="currentpage === 'Cart'"  :cart="cartItems" />
  <Sofa v-if="currentpage === 'Product'" />
  <Contact v-if="currentpage === 'Contact'" />
  <Footer />
</template>
