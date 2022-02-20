<template>
  <section id="head-page">
      <!-- NavBar -->
      <HeaderNavbar :navBar="navBar" />

      <!-- Sub-NavBar -->
      <HeaderImages :navPage="navPage" :headerImages="headerImages"/>
  </section>
</template>

<script>
import HeaderNavbar from "./HeaderNavbar.vue"
import HeaderImages from "./HeaderImages.vue"

export default {
    name: "Header",

    components: {
        HeaderNavbar,
        HeaderImages,
    },

    props: ["navBar", "navPage", "headerImages"],
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