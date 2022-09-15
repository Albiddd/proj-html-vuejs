<template>
    <div class="">
      <div class="card">
        <div class="card-img">
          <img :class="`img${id}`" :src="require(`../assets/svg/${img}`)" alt="">
        </div>
      <div class="info">
        <h5 class="title">{{title}}</h5>
        <p>{{text}}</p>
      </div>
      
  </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CardsComponent',
    props: {
       img: String,
       title: String,
       text: String,
       id: Number
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
  .card{
    text-align: center;

    .card-img{
      background-color:#FAF7F1;
      border-radius: 50%;
      position: relative;
      width: 162px;
      height: 162px;
      margin: 0 auto;
      

      img{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 50px;
      }
      .img0{
        filter: invert(94%) sepia(18%) saturate(284%) hue-rotate(85deg) brightness(90%) contrast(89%);
      }
      .img1{
        filter: invert(88%) sepia(85%) saturate(4456%) hue-rotate(329deg) brightness(98%) contrast(98%);
      }
      .img2{
        filter: invert(30%) sepia(6%) saturate(3896%) hue-rotate(282deg) brightness(96%) contrast(82%);
      }
      .img3{
        filter: invert(48%) sepia(87%) saturate(1886%) hue-rotate(332deg) brightness(103%) contrast(84%);
      }
    }

    .info{

      .title{
        font-weight: 400;
        font-size: 21px;
        line-height: 1.238em;
        padding-top: 20px;
        padding-bottom: 10px;
      }
      p{
        color: rgba(0, 0, 0, 0.651);
        font-size: 16px;
        font-weight: 300;
        line-height: 26px;
      }
    }
  }
  </style>