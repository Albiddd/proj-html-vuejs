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
        </ul>

        <div class="icon">
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
    },
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
    .menu{
        display: flex;

        gap: 28px;
        height: 100%;
        ul{
            display: flex;
            align-items: center;
            height: 100%;
            li{
                height: 100%;
            }
            a{
                width: 100%;
                height: 100%;
                vertical-align: middle;
                padding: 20px 25px;
                font-size: 13px;
                font-weight: 700;
                letter-spacing: .25em;
                text-transform: uppercase;
                color: #000;
                line-height: 14px;
                &:hover div{
                    width: 100%;
                }
                span{
                    position: relative;
                    isolation: isolate;
                    padding: 3px;
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
                    .active{
                        width: 100%;
                    }
                    
                    .nav-el-0{
                        background-color: #F0CEBE;
                    }
                    .nav-el-1{
                        background-color: #E6E2D1;
                    }
                    .nav-el-2{
                        background-color: #D8F0E3;
                    }
                    .nav-el-3{
                        background-color: #EBE8F9;
                    }
                    .nav-el-4{
                        background-color: #FEF2BD;
                    }
                    .nav-el-5{
                        background-color: #FFD9B4;
                    }
                }
            }
        }
    }

  </style>