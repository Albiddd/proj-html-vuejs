<template>
  <div class="jumbotron">
    <div
      class="slider-container"
      @mouseleave="startAutoplay"
      @mouseenter="stopAutoplay"
    >
      <ul class="slides-wrapper">
        <li
          class="slide"
          :class="index == currentSlide ? 'active' : ''"
          v-for="(slide, index) in slides"
          :key="index"
        >
          <div class="col">
            <div class="slide-title">
              {{ slide.title }} <strong>{{ slide.emphasis }}</strong>
            </div>
            <p>{{ slide.caption }}</p>
            <button class="btn">{{ slide.button }}</button>
          </div>
          <div :class="`hero-img${index}`" class="hero-img col">
            <div class="img-wrapper">
              <img
                v-for="(img, i) in slide.imgs"
                :key="i"
                :class="`img${i}`"
                :src="require(`../assets/img/${img}`)"
                alt=""
              />
            </div>
          </div>
        </li>
      </ul>

      <div class="arrows">
        <div class="arrow-prev">
          <font-awesome-icon
            class="arrow-el"
            @click="prevSlide()"
            icon="fa-solid fa-chevron-left"
          />
        </div>
        <div class="arrow-next">
          <font-awesome-icon
            class="arrow-el"
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
          imgs: [
            "short-slider-rev-1-img-3.png",
            "short-slider-rev-1-img-2.png",
            "short-slider-rev-1-img-6.png",
            "short-slider-rev-1-img-1.png",
            "short-slider-rev-1-img-4.png",
            "short-slider-rev-1-img-5.png",
            "short-slider-rev-1-img-7.png",
            "short-slider-rev-1-img-8.png",
            "short-slider-rev-1-img-9.png",
            "short-slider-rev-1-img-10.png",
          ],
        },
        {
          title: "Our new folio full of",
          emphasis: "joy",
          caption:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.",
          button: "Read more",
          imgs: [
            "h-2-slider-img-11.png",
            "short-slider-rev-1-img-2.png",
            "short-slider-rev-1-img-6.png",
            "h-2-slider-img-12.png",
            "h-2-slider-img-13.png",
            "h-2-slider-img-14.png",
          ],
        },
        {
          title: "Devotion that never",
          emphasis: "ends",
          caption:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.",
          button: "Read more",
          imgs: [
            "h-2-slider-img-15.png",
            "h-2-slider-img-16.png",
            "short-slider-rev-1-img-2.png",
            "short-slider-rev-1-img-6.png",
            "h-2-slider-img-12.png",
            "h-2-slider-img-13.png",
            "h-2-slider-img-14.png",
            "h-2-slider-img-17.png",
          ],
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

@import "../style/first-slide.scss" ;
@import "../style/second-slide.scss" ;
@import "../style/third-slide.scss" ;



.slider-container {
  position: relative;
  padding: 80px 0;

  .slides-wrapper {
    max-width: 1350px;
    margin: 0 auto;
    height: 480px;
    .slide {
      display: none;
    }
    .slide.active {
      display: flex;
      align-items: center;
      .col {
        width: 50%;
        .slide-title {
          font-size: 92px;
          font-weight: 300;
          line-height: 1.1;
          strong {
            font-style: italic;
            font-family: "Playfair Display", serif;
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
          padding: 16px 41px;
          font-size: 14px;
          border: 3px solid #e1c0b0;
          transition: linear 0.2s;
          line-height: 22px;
          font-size: 13px;
          font-weight: 700;
          letter-spacing: 0.25em;
          &:hover {
            background-color: #e1c0b0;
            color: white;
          }
        }
      }
    }
  }

  // ARROWS
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
    div {
      background-color: #e1c0b0;
      border-radius: 50%;
      width: 35px;
      height: 35px;
      position: relative;
      .arrow-el {
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