<template>
    <div class="">
      <div class="slider-container"  @mouseleave="startAutoplay" @mouseenter="stopAutoplay">

        <ul class="slides-wrapper">
          <li>
          <!-- <li class="slide" :class="i == currentSlide ? 'active' : '' " 
          v-for="(slide, i) in slides"> -->
            <div>

            </div>
            <div class="hero-img">
              <img src="../assets/img/short-slider-rev-1-img-3.png" alt="">
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
  
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
  </style>