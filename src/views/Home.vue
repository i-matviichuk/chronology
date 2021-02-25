<template>
  <div class="home">
<!--    <img alt="Vue logo" src="../assets/logo.png">-->
<!--    <NavBar/>-->
<!--    <div class="nav">-->
<!--      Home Page-->
<!--    </div>-->
    <MainCarousel/>
  </div>
</template>

<script>
// @ is an alias to /src
// import NavBar from '@/components/NavBar.vue';
import MainCarousel from '../components/MainCarousel.vue';

export default {
  name: 'Home',
  components: {
    // NavBar,
    MainCarousel,
  },
};
</script>
