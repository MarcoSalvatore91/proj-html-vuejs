<template>
  <section>
      <section id="nav-bar-id">
        <div class="nav-bar row align-items-center" v-for="nav in navBar" :key="nav.id">
            <div class="col-2">
                <div class="contain-orange">
                    <a href="#">{{ nav.order }}</a>
                </div>
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
                <a href="#" class="ms-4">{{ nav.search }}</a>
            </div>
        </div>
      </section>
  </section>
</template>

<script>
export default {
    name: "HeaderNavbar",

    props: ["navBar"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

/* Utils */
a {
    text-decoration: $decoration-none;
    font-size: $size-small;
    color: $color-white;
    font-weight: bold;
}

/* Nav-Bar */
#nav-bar-id {

    .contain-orange {
        background-color: $color-orange;
        padding: 10px 0;
        text-align: center;
        width: 120px;
    }

    .nav-bar {
        width: $width-min;
        margin: $content-center;
        
        img {
            width: 200px;
        }
    }
    
    
}
</style>