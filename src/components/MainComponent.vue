<template>
    <div class="">
        <JumboTron/>
        <Illustration/>
        <WorkingProcess/>
        <WorkWithUs/>
        <Articles/>
    </div>
  </template>
  
  <script>
    import JumboTron from './JumboTron.vue';
    import Illustration from './Illustration.vue';
    import WorkingProcess from './WorkingProcess.vue';
    import WorkWithUs from './WorkWithUs.vue';
    import Articles from './Articles.vue';
    
  export default {
    name: "MainComponent",
    props: {},
    components: { JumboTron, Illustration, WorkingProcess, WorkWithUs, Articles },
    data(){
      return{
        processSteps:[
          {
            stepImg: 'icon_lightbulb.svg',
            stepTitle: 'First theres an idea',
            stepText:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.', 
          },
          {
            stepImg: 'icon_comment_alt.svg',
            stepTitle: 'Then we talk about',
            stepText:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.', 
          },
          {
            stepImg: 'icon_cloud.svg',
            stepTitle: 'And we think about',
            stepText:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.', 
          },
          {
            stepImg: 'icon_pens.svg',
            stepTitle: 'So we draw along',
            stepText:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.', 
          }
        ]
      }
    }
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
  </style>
  