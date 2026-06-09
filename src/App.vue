<script>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import Footer from './components/Footer.vue';
import About from './components/About.vue';
import Visit from './components/Visit.vue';
export default{
  components:{
    Navbar,
    Home,
    Footer,
    About,
    Visit
  },
  data(){
    return{
      currentpage: 'Home',
     
    }
  },
  methods:{
    changePage(page){
      this.currentpage = page
    },
    
  }
}
</script>

<template>
<Navbar @switchpages="changePage" />
<Home v-if="currentpage === 'Home' " />
<About v-if="currentpage === 'About' "/>
<Visit v-if="currentpage === 'Visit'" />
<Footer  />
</template>
