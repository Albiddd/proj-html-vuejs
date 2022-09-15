<template>
  <div class="container">
    <div class="row">
      <div class="col" 
      v-for="(article, i) in articles" 
      :key="i">
        <ArticlesCards
          :img="article.artImg"
          :day="article.artDay"
          :date="article.artDate"
          :title="article.artTitle"
          :author="article.artAuthor"
        />
      </div>
    </div>
  </div>
</template>
  
  <script>
import ArticlesCards from "./ArticlesCards.vue";
export default {
  name: "ArticlesSetcion",
  props: {},
  data() {
    return {
      articles: [
        {
          artImg: "h-2-blog-img-1.jpg",
          artTitle: "This way, loves: a detailed guide through new design",
          artAuthor: "Emily Fields",
          artDay: "07",
          artDate: "May '19",
        },
        {
          artImg: "h-2-blog-img-2.jpg",
          artTitle: "I try to give people a different way of looking art",
          artAuthor: "Emily Fields",
          artDay: "07",
          artDate: "May '19",
        },
        {
          artImg: "h-2-blog-img-3.jpg",
          artTitle: "Introduce Richard Laperrière of those amazing features",
          artAuthor: "Emily Fields",
          artDay: "07",
          artDate: "May '19",
        },
      ],
    };
  },
  components: { ArticlesCards },
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">

    .container{
      max-width: 1300px;
      margin: 0 auto;
      padding-top: 150px;
      padding-bottom: 139px;
      .row{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 30px;
        .col{
          flex-basis: calc(100% / 3);
        }
      }
    }

</style>