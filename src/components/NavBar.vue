<template>
    <div class="menu">
        
        <ul class="nav">
            <li v-for="(element, i) in menu" 
            :key="i" class="menu-link">
            <a href="#">{{element}}</a>
            </li>
            <!-- <ul class="dropdown">
                <li v-for="(el, i) in drops" :key="i" class="dropdown-el">{{el}}</li>
            </ul>             -->
        </ul>

        <div class="">
            <a href="#"><img src="../assets/svg/svg-1.svg" alt="menu"></a>
        </div>

    </div>
  </template>
  
  <script>
  export default {
    name: 'NavBar',
    props: {
        
    },
    data(){
        return{
            menu : ['Home', 'Pages', 'Portfolio', 'Blog', 'Shop', 'Elements'],
        }
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
    .menu{
        display: flex;
        gap: 20px;
        ul{
            display: flex;
            a{
                padding: 0 30px;
                text-transform: uppercase;
                color: black;
                font-weight: 600;
                font-size: 14px;
            }
        }
    }

  </style>