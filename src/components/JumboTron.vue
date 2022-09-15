<template>
  <div class="">
    <div
      class="slider-container"
      @mouseleave="startAutoplay"
      @mouseenter="stopAutoplay"
    >
      <ul class="slides-wrapper">
        <li class="slide" :class="index == currentSlide ? 'active' : '' " 
        v-for="(slide, index) in slides" :key="index">
          <div class="col">
            <div class="slide-title">
              {{ slide.title }} <strong>{{ slide.emphasis }}</strong>
            </div>
            <p>{{ slide.caption }}</p>
            <button class="btn">{{ slide.button }}</button>
          </div>
          <div class="hero-img col">
            <img :src="require(`../assets/img/${slide.img}`)" alt="" />
          </div>
        </li>
      </ul>

      <div class="arrows">
        <div class="arrow-prev">
          <font-awesome-icon class="arrow-el"
            @click="prevSlide()"
            icon="fa-solid fa-chevron-left"
          />
        </div>
        <div class="arrow-next">
          <font-awesome-icon class="arrow-el"
            @click="nextSlide()"
            icon="fa-solid fa-chevron-right"
          />
        </div>
      </div>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "JumboTron",
  props: {},
  data() {
    return {
      slides: [
        {
          title: "Projects made with",
          emphasis: "love",
          caption:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.",
          button: "Read more",
          img: "short-slider-rev-1-img-3.png",
        },
        {
          title: "Our new folio full of",
          emphasis: "joy",
          caption:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.",
          button: "Read more",
          img: "h-2-slider-img-11.png",
        },
        {
          title: "Devotion that never",
          emphasis: "ends",
          caption:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.",
          button: "Read more",
          img: "h-2-slider-img-15.png",
        },
      ],
      currentSlide: 0,
      intervall: null,
    };
  },
  methods: {
    nextSlide() {
      this.currentSlide++;
      if (this.currentSlide > this.slides.length - 1) {
        this.currentSlide = 0;
      }
    },
    prevSlide() {
      this.currentSlide--;
      if (this.currentSlide < 0) {
        this.currentSlide = this.slides.length - 1;
      }
    },
    startAutoplay() {
      this.interval = setInterval(this.nextSlide, 5000);
    },
    stopAutoplay() {
      clearInterval(this.interval);
    },
  },
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
.slider-container {
  position: relative;
  padding: 50px 0;
  .slides-wrapper {
    max-width: 1350px;
    margin: 0 auto;
    .slide{
      display: none;
    }
    .slide.active {
      display: flex;
      align-items: center;
      .col {
        width: 50%;
        .slide-title {
          font-size: 92px;
          font-weight: 200;
          line-height: 1.1;
          strong {
            font-style: italic;
            font-family: 'Playfair Display', serif;
          }
        }
        p {
          font-size: 20px;
          font-weight: 300;
          margin: 20px 0;
        }
        button {
          text-transform: uppercase;
          font-weight: 600;
          background-color: #fff;
          padding: 12px 35px;
          font-size: 14px;
          border: 3px solid #e1c0b0;
          transition: linear 0.2s;
          &:hover {
            background-color: #e1c0b0;
            color: white;
          }
        }
      }
    }
  }

  .arrows {
    display: flex;
    justify-content: space-between;
    padding: 0 20px;
    font-size: 1.75rem;
    position: absolute;
    top: 50%;
    left: 0;
    right: 0;
    transform: translateY(-50%);
    color: white;
    div{
      background-color: #e1c0b0;
      border-radius: 50%;
      width: 35px;
      height: 35px;
      position: relative;
      .arrow-el{
        font-size: 25px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
    }
  }
}
</style>