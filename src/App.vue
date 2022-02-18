<template>
  <div id="app">
    <Header :navBar="navBar" :navPage="navPage" :headImage="headImage"/>
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",

  components: {
    Header,
    Main,
    Footer,
  },

  data() {
    return {

      navBar: [{
        order: "ORDER ONLINE",
        home: "HOME",
        pages: "PAGES",
        menu: "MENU",
        image: "h5-logo-divided-header.png",
        event: "EVENT",
        blog: "BLOG",
        landing: "LANDING",
        cart: "CART",
        search: "SEARCH",
      }],

      navPage: [{
        prev: "PREV",
        next: "NEXT",
      }],

      headImage: [{
        bgImage: "h3-rev-img-",
        image: "h3-rev-img-"
      }]
    }
  }
};
</script>

<style lang="scss">
@import './assets/scss/style.scss';

</style>
