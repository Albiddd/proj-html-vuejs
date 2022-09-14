<template>
    <div class="wrapper">
      <div class="col" v-for="el, i in illustrations" :key="i">
        <img :src="require(`../assets/img/${el}`)" alt="">
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
        'h-2-port-img-1.jpg', 
        'h-2-port-img-2.jpg', 
        'h-2-port-img-3.jpg', 
        'h-2-port-img-4.jpg', 
        'h-2-port-img-5.jpg', 
        'h-2-port-img-6.jpg', 
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
        img{
          display: block;
          width: 100%;
        }
      }
    }
  </style>