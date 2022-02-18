<template>
  <section id="head-page">
      <!-- NavBar -->
      <section id="nav-bar-id">
        <div class="nav-bar row align-items-center" v-for="nav in navBar" :key="nav.id">
            <div class="col-2">
                <a href="#">{{ nav.order }}</a>
            </div>

            <div class="col-8 d-flex align-items-center justify-content-between">
                <a href="#">{{ nav.home }}</a>
                <a href="#">{{ nav.pages }}</a>
                <a href="#">{{ nav.menu }}</a>
                <img :src="require (`../assets/img/${nav.image}`)" alt="">
                <a href="#">{{ nav.event }}</a>
                <a href="#">{{ nav.blog }}</a>
                <a href="#">{{ nav.landing }}</a>
            </div>

            <div class="col-2 d-flex align-items-center justify-content-end">
                <a href="#">{{ nav.cart }}</a>
                <a href="#">{{ nav.search }}</a>
            </div>
        </div>
      </section>

      <!-- Sub-NavBar -->
      <section id="sub-navbar" class="row justify-content-between">
        <div class="col-2 d-flex align-items-center">
            <a href="#">{{ navPage[0].prev }}</a>
        </div>

        <div class="col-8 d-flex justify-content-center" v-for="image in headImages" :key="image.id">
            <img :src="require (`../assets/img/${image.image}5.png`)" alt="">
            <img class="img-pizza-header" :src="require (`../assets/img/${image.image}6.png`)" alt="">
        </div>

        <div class="col-2 d-flex justify-content-end align-items-center">
            <a href="#">{{ navPage[0].next }}</a>
        </div>
      </section>
  </section>
</template>

<script>
export default {
    name: "Header",

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

/* Utils */

a {
    text-decoration: $decoration-none;
}

/* Nav-Bar */
#nav-bar-id {

    .nav-bar {
        width: $width-min;
        margin: $content-center;
    }
    
    img {
        width: 200px;
    }
    
}

/* Sub-NavBar */

#sub-navbar {
    padding-top: 30px;
    padding-bottom: 100px;
    position: relative;
}

.img-pizza-header {
    position: absolute;
}

</style>