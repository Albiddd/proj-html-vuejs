<template>
      <div class="list">
        <div class="col">
         <ul>
            <li>{{firstItem}}</li>
            <li v-if="index !== 2" >{{secondItem}}</li>
            <li class="social-row" v-else>
                <font-awesome-icon class="social-icon"
                v-for="(icon, i) in social"
                :key="i"
                :icon="icon"
                 />         
            </li>
         </ul>
        </div>
      </div>
  </template>
    
    <script>
  export default {
    name: "FooterList",
    props: {
        firstItem: String,
        secondItem: String,
        index: Number,
        social: Array
    },

  };
  </script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped lang="scss">
    
    .col{
        flex-basis: calc(100% / 4);
        li{
            padding-bottom: 15px;
        }
    }

    .social-row{
        display: flex;
        justify-content: space-between;
        .social-icon{
            cursor: pointer;
        }
    }
    
    
  </style>