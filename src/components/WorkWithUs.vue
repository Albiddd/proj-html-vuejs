<template>
  <div class="section-bg">
    <div class="container">
      <div class="title">
        Want to work with us? Send us
        <strong>a message!</strong>
      </div>
      <p class="text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore. Ut enim ad minim veniam, quis
        nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.
      </p>
      <button class="btn">contact</button>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "WorkWithUs",
  props: {},
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
.section-bg {
  background-image: url("https://maree.qodeinteractive.com/wp-content/uploads/2019/05/h-2-background-1.jpg?id=589");
  background-repeat: no-repeat;
  background-size: cover;
  // height: 529px;
  // margin-top: 180px;
}

.container {
  padding: 114px 16% 119px 16%;
  text-align: center;
  .title {
    font-size: 65px;
    line-height: 1.261em;
    strong {
      font-style: italic;
      font-family: "Playfair Display", serif;
    }
  }
  .text {
    color: rgba(0, 0, 0, 0.651);
    font-size: 20px;
    line-height: 30px;
    font-weight: 300;
    margin-top: 23px;
    margin-block: 37px;
  }
  .btn{
    font-size: 13px;
    line-height: 1.8em;
    letter-spacing: .25em;
    font-weight: 700;
    text-transform: uppercase;
    background-color: #D8F0E3;
    padding: 17px 70px;
    border: none;
    transition: linear 0.2s;
    &:hover{
      background-color: #e1c0b0;
      color: white;
    }
  }
}
</style>