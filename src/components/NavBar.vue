<template>
    <div class="menu">
        
        <ul class="nav">
            <li v-for="(element, i) in menu" 
            :key="i" class="menu-link">
            <a href="#">
                <span>
                    {{element}}
                    <div :class="`nav-el-${i}`"></div>
                </span>
            </a>
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
        gap: 28px;
        ul{
            display: flex;
            align-items: center;
            height: 100%;
            a{
                width: 100%;
                height: 100%;
                vertical-align: middle;
                padding: 0 25px;
                font-size: 13px;
                font-weight: 700;
                letter-spacing: .25em;
                text-transform: uppercase;
                color: #000;
                line-height: 14px;
                span{
                    position: relative;
                    isolation: isolate;
                    div{
                        width: 0;
                        height: 6px;
                        z-index: -1;                       
                        display: block;
                        transition: width 0.2s;
                        position: absolute;
                        bottom: 2px;
                        left: 0;
                    }
                    &:hover div{
                        width: 100%;
                    }
                    &:hover .nav-el-0{
                        background-color: #F0CEBE;
                    }
                    &:hover .nav-el-1{
                        background-color: #E6E2D1;
                    }
                    &:hover .nav-el-2{
                        background-color: #D8F0E3;
                    }
                    &:hover .nav-el-3{
                        background-color: #EBE8F9;
                    }
                    &:hover .nav-el-4{
                        background-color: #FEF2BD;
                    }
                    &:hover .nav-el-5{
                        background-color: #FFD9B4;
                    }
                }
            }
        }
    }

  </style>