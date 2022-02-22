<template>
  <div id="app">
    <Header :navBar="navBar" :navPage="navPage" :headerImages="headerImages"/>
    <Main :navPage="navPage" />
    <Footer :restaurants="restaurants" :openDays="openDays" :footerText="footerText"/>
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

      /* Header */
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

      headerImages: [{
        image: "h3-rev-img-"
      }],

      /* Footer */
      restaurants: [
        {
          road: "1614 E. Bell Rd #104.",
          place: "Salerno, AZ 85022",
          number: "(602) 867-1010"
        },
        {
          road: "204 E. Pizzetta Tommaso",
          place: "Sorrento, AZ 85022",
          number: "(358) 867-1010"
        },
        {
          road: "Vale Puglia 54",
          place: "Torre Del Greco",
          number: "(359) 867-1010"
        },
        {
          road: "Corso Itali AA",
          place: "Naples, AZ 85022",
          number: "(989) 867-1010"
        },
      ],

      openDays : [
        {
          day: "MONDAY",
          openHour: "Kitchen Closed"
        },
        {
          day: "TUESDAY UNTIL FRIDAY",
          openHour: "9:00 - 22-00"
        },
        {
          day: "SATURDAY*",
          openHour: "Saturday 11am to midnight"
        },
        {
          day: "Sunday",
          openHour: "9:00 - 22:00"
        },
      ],

      footerText : [
        {
        text: "THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.",
        },
      ]
    }
  }
};
</script>

<style lang="scss">
@import './assets/scss/style.scss';

* {
  overflow-x: hidden;
}

</style>
