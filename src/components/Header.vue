<template>
  <section id="head-page">
      <!-- NavBar -->
      <HeaderNavbar :navBar="navBar" />

      <!-- Sub-NavBar -->
      <HeaderSub :navPage="navPage" :headImages="headImages"/>
  </section>
</template>

<script>
import HeaderNavbar from "./HeaderNavbar.vue"
import HeaderSub from "./HeaderSub.vue"

export default {
    name: "Header",

    components: {
        HeaderNavbar,
        HeaderSub,
    },

    props: ["navBar", "navPage", "headImages"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

/* Generics */

#head-page{
    background-color: $bgc-black;
    padding: 40px 0;
}

</style>