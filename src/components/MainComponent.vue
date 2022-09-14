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
    components: { JumboTron, Illustration, WorkingProcess, WorkWithUs, Articles }
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  
  </style>
  