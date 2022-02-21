<template>
    <section>
        <section id="sub-navbar" class="row justify-content-between">
            <div id="btn-prev" class="col-2 d-flex align-items-center">
                <div class="prev-position rounded-circle">
                    <a href="#" class="prev">{{ navPage[0].prev }}</a>
                </div>
            </div>

            <div class="col-8 d-flex justify-content-center" v-for="image in headerImages" :key="image.id">
                <img :src="require (`../assets/img/${image.image}5.png`)" alt="">
                <img class="img-pizza-header" :src="require (`../assets/img/${image.image}6.png`)" alt="">
            </div>

            <div id="btn-next" class="col-2 d-flex justify-content-end align-items-center">
                <div class="next-position rounded-circle">
                    <a href="#" class="next">{{ navPage[0].next }}</a>
                </div>
            </div>
        </section>
    </section>
</template>

<script>
export default {
    name: "HeaderImages",

    props: ["navPage", "headerImages"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

/* Utils */

a {
    text-decoration: $decoration-none;
    font-size: $size-small;
    color: $color-orange;
    font-weight: bold;
}

/* Sub-NavBar */



#sub-navbar {
    padding-top: 30px;
    padding-bottom: 100px;
    position: relative;

    #btn-prev {
        .prev-position {
            position: relative;
            left: -50px;
            transform: rotate(90deg);
            padding: 30px;
            background-color: $color-white;
            .prev {
                position: relative;
                bottom: 25px;
            }
        }
    }
    #btn-next {
        .next-position {
            position: relative;
            right: -50px;
            transform: rotate(270deg);
            padding: 30px;
            background-color: $color-white;
            .next {
                position: relative;
                bottom: 25px;
            }
        }
    }
    .next {
        transform: rotate(270deg);
    }
}

.img-pizza-header {
    position: absolute;
}
</style>