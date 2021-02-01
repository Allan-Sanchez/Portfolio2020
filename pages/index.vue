<template>
  <div class="container-father">
    <style>
      :root{
        --backgroundColor:{{ backgroundColor }};
        --colortest:{{ colorTest }};
        --primary-color:{{ primaryColor }};
        --primary-clor2:{{primaryColor2}};
        --title-color: {{ titleColor }};
        --text-color: {{ textColor }};
        --border-color: {{ borderColor }};
        --shadow-color:  {{ shadowColor }};
        --box-shadow: {{ boxShadowColor }};
        --gradient-color: {{ gradienColor }};
        --roboto:{{ fontRoboto }}; 
        --background-navbar:{{ backgroundNavbar }}; 
        --shadow-navbar:{{ shadowNavbar }}; 
        --border-navbar:{{ borderNavbar }}; 
        
      }
    </style>
    <!-- Menu Navagetion -->
    <NavBar @Changemode="modeChange()"></NavBar>

    <main class="site-main dark " id="section-home">
        <!-- Banner Hero -->
        <Banner></Banner>

        <!-- about me -->
        <Abouts></Abouts>

        <!-- timeline -->
        <Skill></Skill>

        <!-- contact -->
        <Contact></Contact>




     
    
    </main>

    <!-- <h6>{{$t('hello')}}</h6> -->
  </div>
</template>

<script>
import NavBar from '~/components/Navbar2.vue';
import Banner from '~/components/Banner.vue';
import Abouts from '~/components/Abouts.vue';
import Skill from '~/components/Skill.vue';
import Contact from '~/components/Contact.vue';



export default {
  components: {
    NavBar,
    Banner,
    Abouts,
    Skill,
    Contact
  },
  data() {
    return {
      mode:'light',
      backgroundColor:'#f3f7f9',
      colorTest:'#f00',
      primaryColor: '#4458dc',
      primaryColor2: '#854fee',
      titleColor: '#141313',
      textColor: '#000000',
      borderColor: '#201f1f17',
      shadowColor: '0px 10px 30px rgba(118,85,225,03)',
      boxShadowColor: '0px 10px 30px rgba(57,56,61,0.205)',
      gradienColor: 'linear-gradient(90deg, #4458dc 0%,#854fee 100%)',
      fontRoboto: "'Roboto',cursive",
      backgroundNavbar:'#fff',
      shadowNavbar:'rgba(37,38,94,0.06)',
      borderNavbar:'#d3dce6'

    }
  },
  methods: {
    modeChange(){
      if (this.mode === 'light') {
        this.backgroundColor = '#0d2438';
        this.titleColor = '#ccc';
        this.textColor= '#fff';
        this.backgroundNavbar ="#15334d";
        this.shadowNavbar="rgba(129, 130, 221, 0.06)";
        this.borderNavbar="#1d4364";
        this.mode = 'dark';
      }else{
        this.borderNavbar="#d3dce6";
        this.backgroundNavbar ="#fff";
        this.shadowNavbar="rgba(37,38,94,0.06)";
        this.backgroundColor='#f3f7f9',
        this.colorTest='#f00',
        this.primaryColor= '#4458dc',
        this.primaryColor2= '#854fee',
        this.titleColor= '#141313',
        this.textColor= '#000000',
        this.borderColor= '#201f1f17',
        this.shadowColor= '0px 10px 30px rgba(118,85,225,03)',
        this.boxShadowColor= '0px 10px 30px rgba(57,56,61,0.205)',
        this.gradienColor= 'linear-gradient(90deg, #4458dc 0%,#854fee 100%)',
        this.fontRoboto= "'Roboto',cursive"
        this.mode = 'light'
      }
    }
  },
}
</script>

<style >
 
  body{
    
    background: var(--backgroundColor);
  }

  p.para{
  color: var(--text-color);
  font: normal 500 16px/25px var(--roboto);    
  }

</style>