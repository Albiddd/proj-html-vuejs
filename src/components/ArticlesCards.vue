<template>
  <div class="card-container">
    <div class="card">
      <div class="img">
        <img :src="require(`../assets/img/${img}`)" alt="" />
      </div>
      <div class="datebox">
          <div class="box-top">{{ day }}</div>
          <div class="box-bottom">{{ date }}</div>
        </div>
      <h4 class="title">{{ title }}</h4>
      <div class="credits">By {{ author }}</div>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "ArticlesCards",
  props: {
    img: String,
    title: String,
    author: String,
    day: String,
    date: String,
  },
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">

.img {
  overflow: hidden;
  img {
    display: block;
    width: 100%;
    transition: linear 0.2s;
    &:hover{
        transform: scale(1.03);
    }
  }
}

.card{
    position: relative;
  .datebox {
    position: absolute;
    top: -15px;
    left: 15px;
    z-index: 99;
    font-weight: 700;
    width: 65px;
    filter: drop-shadow(0 2px 2px rgba(0, 0, 0, .05));

    .box-top {
      font-family: "Playfair Display", serif;
      color: #000;
      font-size: 34px;
      font-style: italic;
      text-align: center;
      background-color: #c0e1cf;
      vertical-align: middle;
      padding-top: 0;  

    }
    .box-bottom {
      background-color: #f3d0c7;
      width: 100%;
      height: 38px;
      clip-path: polygon(0 0, 100% 0, 100% 100%, 50% 70%, 0 100%);
      padding: 4px 1px;
      text-transform: uppercase;
      color: #000;
      font-size: 11px;
      text-align: center;
      letter-spacing: 1.1px;
    }
  }
}

.title{
    color: #000;
    font-weight: 400;
    margin: 15px 0;
    word-wrap: break-word;
    font-size: 26px;
    line-height: 1.231em;
}
.credits{
    color: #000;
    font-size: 15px;
    line-height: 1.267em;
    font-family: "Playfair Display", serif;
    font-style: italic;
    font-weight: 300;
}

</style>