<template>
  <div id="app" style="height: 4000px">
    <TopNav></TopNav>
    <SerchNav></SerchNav>
    <NavigationBar></NavigationBar>
    <Banner></Banner>
    <Commodity style="clear: both"></Commodity>
    <Special></Special>
    <Maternal></Maternal>
    <Makeup></Makeup>
    <Life></Life>
    <Like></Like>
    <Footer></Footer>
  </div>
</template>

<script>

  import TopNav from './Top_Nav.vue'
  import SerchNav from './SerchNav/SerchNav'
  import NavigationBar from './NavigationBar/NavigationBar'
  import Banner from './Banner/Banner'
  import Commodity from './Content/Commodity'
  import Special from './Special/Special'
  import Maternal from './Maternal/Maternal'
  import Makeup from './Makeup/Makeup'
  import Life from './Life/Life'
  import Like from './Like/Like'
  import Footer from './Footer/Footer'







  export default {
        name: "App",
      components:{
          TopNav,
          SerchNav,
        NavigationBar,
        Banner,
        Commodity,
        Special,
        Maternal,
        Makeup,
        Life,
        Like,
        Footer
      }
    }
</script>

<style scoped lang="less">
@import "static/css/common";

</style>
