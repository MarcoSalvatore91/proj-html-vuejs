<template>
    <section>
        <section id="sub-navbar" class="row justify-content-between">
            <div id="btn-prev" class="col-2 d-flex align-items-center">
                <div class="prev-position rounded-circle">
                    <button @click="prevPage()" class="prev btn">{{ navPage[0].prev }}</button>
                </div>
            </div>

            <div class="col-8 d-flex justify-content-center" v-for="image in headerImages" :key="image.id">
                <img :src="require (`../assets/img/${image.image}5.png`)" alt="">
                <img class="img-pizza-header" :src="require (`../assets/img/${image.image}${currentIndex}.png`)" alt="">
            </div>

            <div id="btn-next" class="col-2 d-flex justify-content-end align-items-center">
                <div class="next-position rounded-circle">
                    <button @click="nextPage()" class="next btn">{{ navPage[0].next }}</button>
                </div>
            </div>
        </section>
    </section>
</template>

<script>
export default {
    name: "HeaderImages",

    props: ["navPage", "headerImages"],

    data() {
        return {
            currentIndex: 6,
        }
    },

    methods: {
        prevPage() {
            this.currentIndex -= 2;
            if(this.currentIndex === 0) {
                return this.currentIndex = 6;
            }
        },

        nextPage() {
            this.currentIndex += 2;
            if(this.currentIndex > 6) {
                return this.currentIndex = 2;
            }
        }
    }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

section {
    overflow: hidden;
}

/* Utils */

.btn {
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
            left: -70px;
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
            right: -110px;
            padding: 45px;
            background-color: $color-white;
            .next {
                position: relative;
                right: 50px;
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