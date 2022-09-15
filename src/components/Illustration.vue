<template>
    <div class="wrapper">
      <div class="col" v-for="el, i in illustrations" :key="i">
        <img :src="require(`../assets/img/${el.img}`)" alt="">
        <div class="details">
          <h4 class="title">{{ el.title }}</h4>
          <div class="text">{{ el.text }}</div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'IllustrationSection',
    props: {
  
    },
    data(){
      return{
        illustrations:[ 
          {
            img:'h-2-port-img-1.jpg', 
            title: 'All these illustrations',
            text: 'Illustration'
          },
          {
            img:'h-2-port-img-2.jpg', 
            title: 'Type and Illustrations',
            text: 'Illustration'
          },
          {
            img:'h-2-port-img-3.jpg', 
            title: 'Draw and illustrate',
            text: 'Illustration'
          },
          {
            img:'h-2-port-img-4.jpg', 
            title: 'Illustrations of novels',
            text: 'Illustration'
          },
          {
            img:'h-2-port-img-5.jpg', 
            title: 'Too many illustrations',
            text: 'Illustration'
          },
          {
            img:'h-2-port-img-6.jpg', 
            title: 'Dreams are illustrations',
            text: 'Illustration'
          }
        ]
      }
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
    .wrapper{
      display: flex;
      flex-wrap: wrap;
      gap: 0px;
      padding: 30px 0;
      .col{
        flex-basis: calc(100%/3);
        position: relative;
        overflow: hidden;
        img{
          display: block;
          width: 100%;
        }

        .details{
          position: absolute;
          display: block;
          width: auto;
          max-width: 88%;
          height: auto;
          top: 50%;
          padding: 23px 32px 32px;
          background-color: #fff;
          opacity: 0;
          overflow: hidden;
          transform: translateX(-200px) translateY(-50%);
          transition: .3s;
          will-change: unset;
        }
        &:hover .details{
          opacity: 1;
          transform: translateX(0px) translateY(-50%);
        }
        .title{
          font-size: 26px;
          line-height: 1.231em;
          font-weight: 400;
        }
        .text{
          font-style: italic;
          font-family: 'Playfair Display', serif;
        }
      }
    }
  </style>