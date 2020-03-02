<template>
  <div>
    <full-page :options="options" id="fullpage" ref="fullpage">
      <first-page></first-page>
      <second-page></second-page>
      <third-page></third-page>
      <fourth-page></fourth-page>
    </full-page>
  </div>
</template>

<script>
  import './fullpage.js'
  import FirstPage from '../section1/Page.vue'
  import SecondPage from '../section2/Page.vue'
  import ThirdPage from '../section3/Page.vue'
  import FourthPage from '../section4/Page.vue'

  export default {
    name: 'VueFullPage',
    components: {
      FirstPage,
      SecondPage,
      ThirdPage,
      FourthPage
    },
    data() {
      return {
        options: {
          licenseKey: 'OPEN-SOURCE-GPLV3-LICENSE',
          afterLoad: this.afterLoad,
          navigation: true, //是否显示导航，默认为false
          navigationPosition: 'right', //导航小圆点的位置
          // anchors: ['page1', 'page2', 'page3'],
          paddingTop: "50px",
          sectionsColor: [
            '#41b883',
            '#ff5f45',
            '#0798ec'
          ]
        }
      };
    },
    methods: {
      afterLoad: function (origin, destination, direction) {
        console.log('After load....');
        console.log(destination);
      }
    }
  };
</script>

<style>


</style>