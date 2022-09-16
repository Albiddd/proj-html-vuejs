<template>
    <header>
        <div class="logo">
            <img src="../assets/img/logo-sidearea-1.png" alt="">
        </div>
        <div class="nav">
          <NavBar/>
        </div>
    </header>
  </template>
  
  <script>
import NavBar from './NavBar.vue';
  export default {
    name: "MainHeader",
    props: {},
    components: { NavBar }
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
    
    header{
      background-color: white;
      padding: 0 40px;
      height: 100px;
      display: flex;
      justify-content: space-between;
      align-items: center;

    }

  </style>
  