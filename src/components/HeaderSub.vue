<template>
    <section>
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
    name: "HeaderSub",

    props: ["navPage", "headImages"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

/* Utils */

a {
    text-decoration: $decoration-none;
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