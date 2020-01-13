<template>
  <div class="container-father">
    <NavBar></NavBar>

    <!-- <h6>{{$t('hello')}}</h6> -->
  </div>
</template>

<script>
import NavBar from '~/components/Navbar.vue';

export default {
  components: {
    NavBar
  }
}
</script>

<style >
  :root{
    --primary-color:#4458dc;
    --primary-clor2: #854fee;
    --title-color: #141313;
    --text-color: #777777;
    --border-color: #201f1f17;
    --shadow-color:  0px 10px 30px rgba(118,85,225,03);
    --box-shadow: 0px 10px 30px rgba(57,56,61,0.205);
    --gradient-color: linear-gradient(90deg, #4458dc 0%,#854fee 100%);

    --roboto:'Roboto',cursive;
  }
</style>