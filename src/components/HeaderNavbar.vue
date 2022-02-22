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
                <div>
                    <img class="svg pe-2" src="../assets/svg/svg-0.svg" alt="mustache">
                    <a href="#">{{ nav.home }}</a>
                </div>
                <a href="#">{{ nav.pages }}</a>
                <a href="#">{{ nav.menu }}</a>
                <img class="logo" :src="require (`../assets/img/${nav.image}`)" alt="">
                <a href="#">{{ nav.event }}</a>
                <a href="#">{{ nav.blog }}</a>
                <a href="#">{{ nav.landing }}</a>
            </div>

            <div class="col-2 d-flex align-items-center justify-content-end">
                <div>
                    <img class="cart svg pe-2" src="../assets/svg/svg-1.svg" alt="cart">
                    <a class="pe-4" href="#">{{ nav.cart }}</a>
                </div>
                <div>
                    <i class="fa-solid fa-magnifying-glass"></i>
                    <a href="#" class="ms-4">{{ nav.search }}</a>
                </div>
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

.svg {
    height: 10px;
    filter: invert(100%) sepia(0%) saturate(7494%) hue-rotate(25deg) brightness(97%) contrast(99%);

}

.cart {
    height: 20px;
}

i {
    margin-right: -15px;
    color: white;
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
        
        .logo {
            width: 200px;
        }
    }
    
    
}
</style>