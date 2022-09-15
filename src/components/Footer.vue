<template>
  <footer>
    <div class="container">
      <div class="col">
        <div class="logo-box">
          <img src="../assets/img/logo-sidearea-1.png" alt="">
          <div class="text"> Let's Get Creative</div>
        </div>
      </div>
      <FooterList
      v-for="(item, i) in items"
      :key="i"
      :firstItem="item.firstItem"
      :secondItem="item.secondItem"
      :index="i"
      :social="item.socials"
      />
    </div>
  </footer>
</template>
  
  <script>
import FooterList from './FooterList.vue';

export default {
    name: "MainFooter",
    props: {},
    data() {
        return {
          items:[
            {
              firstItem: 'maree@qodeinteractive.com',
              secondItem: '+44645 321 789'
            },
            {
              firstItem: 'Avenue d\'Auderghem 10',
              secondItem: '1040 Brussels, Belgium'
            },
            {
              firstItem: 'Stay in touch with us',
              socials:[
                'fa-brands fa-twitter',
                'fa-brands fa-pinterest-p',
                'fa-brands fa-facebook-f',
                'fa-brands fa-linkedin-in']
            }
          ]
        };
    },
    components: { FooterList }
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  footer{
    background-color: #C0E1CF;
    font-size: 16px;
    font-weight: 300;
    line-height: 26px;
  }
  .container {
    max-width: 1300px;
    margin: 0 auto;
    padding: 73px 15px 78px 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .col{
      flex-basis: calc(100% / 4);
    }
    .logo-box{
      img{
        padding-bottom: 12px;
      }
      div{
        padding-bottom: 15px;
      }
    }
  }
</style>