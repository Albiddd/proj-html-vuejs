<template>
    <div class="">
      <div class="slider-container"  @mouseleave="startAutoplay" @mouseenter="stopAutoplay">

        <ul class="slides-wrapper">
          <li v-for="(slide, index) in slides" :key="index" >
            
          <!-- <li class="slide" :class="i == currentSlide ? 'active' : '' " 
          v-for="(slide, i) in slides"> -->
            <div class="col">
              <div class="slide-title">{{slide.title}} <strong>{{slide.emphasis}}</strong> </div>
              <p>{{slide.caption}}</p>
              <button class="btn">{{slide.button}}</button>
            </div>
            <div class="hero-img col">
              <img :src="require(`../assets/img/${slide.img}`)" alt="">
            </div>
          </li>
          
        </ul>

        <!-- <div class="arrows">
          <p class="arrow-prev">
            <i @click="prevSlide" class="fa-solid fa-chevron-left"></i>
          </p>
          <p class="arrow-next">
            <i @click="nextSlide" class="fa-solid fa-chevron-right"></i>
          </p>
        </div> -->

      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'JumboTron',
    props: {
  
    },
    data(){
      return{
        slides:[
          {
            title: 'Projects made with',
            emphasis:'love',
            caption: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
            button: 'Read more',
            img: 'short-slider-rev-1-img-3.png'
          },
          {
            title: 'Our new folio full of',
            emphasis:'joy',
            caption: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
            button: 'Read more',
            img: 'h-2-slider-img-11.png'
          },
          {
            title: 'Devotion that never',
            emphasis:'ends',
            caption: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
            button: 'Read more',
            img: 'h-2-slider-img-15.png'
          }        
        ],
        currentSlide: 0,
		    interval: null,
      }
    },
    methods:{

    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">

    .slides-wrapper{
      max-width: 1350px;
      margin: 0 auto;
      li{
        display: flex;
        align-items: center;
        .col{
          width: 50%;
          .slide-title{
            font-size: 92px;
            font-weight: 300;
            line-height: 1.1;
            strong{
              font-style: italic;
              font-family: 'Times New Roman', Times, serif;
            }
          }
          p{
            font-size: 20px;
            font-weight: 300;
            margin: 20px 0;
          }
          button{
            text-transform: uppercase;
            font-weight: 600;
            background-color: #fff;
            padding: 12px 35px;
            font-size: 14px;
            border: 3px solid #e1c0b0;
            &:hover{
              background-color: #e1c0b0;
              color: white;
            }
          }
        }
      }
    }

  </style>