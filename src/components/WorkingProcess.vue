<template>
  <div class="container">
    <div class="section-title">Working <strong>process</strong></div>

    <div class="stacked">
      <div class="row">
        <Cards
          class="col"
          v-for="(item, i) in processItems"
          :key="i"
          :id="i"
          :img="item.itemImg"
          :title="item.itemTitle"
          :text="item.itemText"
        />
      </div>
  
      <img src="../assets/svg/svg-3.svg" alt="wave" />
    </div>

  </div>
</template>
  
<script>
import Cards from "./Cards.vue";
export default {
  name: "WorkingProcess",
  props: {},
  data() {
    return {
      processItems: [
        {
          itemImg: "icon_lightbulb.svg",
          itemTitle: "First theres an idea",
          itemText:
            "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.",
        },
        {
          itemImg: "icon_comment_alt.svg",
          itemTitle: "Then we talk about",
          itemText:
            "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.",
        },
        {
          itemImg: "icon_cloud.svg",
          itemTitle: "And we think about",
          itemText:
            "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.",
        },
        {
          itemImg: "icon_pens.svg",
          itemTitle: "So we draw along",
          itemText:
            "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.",
        },
      ],
    };
  },
  components: { Cards },
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
    
    .container{
      max-width: 1300px;
      margin: 90px auto;
      text-align: center;
      .section-title{
        font-size: 65px;
        line-height: 65px;
        
        strong{
          font-style: italic;
          font-family: "Playfair Display",serif;
        }
      }
      .row{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 60px;
        .col{
          flex-basis: calc(100%/ 4);
        }
      }
    }
    .stacked{
      position: relative;
      margin: 90px 0;
      img{
        display: block;
        position: absolute;
        top: 0;
        left: 50%;
        transform: translateX(-50%);
        z-index: -1;
      }
    }

</style>