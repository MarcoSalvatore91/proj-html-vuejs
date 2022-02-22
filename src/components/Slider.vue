<template>
  <section id="slider" class="my-2">
    <section id="content" class="row justify-content-between">
        <div id="btn-prev" class="col-2 d-flex align-items-center">
            <div class="prev-position rounded-circle">
                <button @click="prevPage()" class="prev btn">{{ navPage[0].prev }}</button>
            </div>
        </div>

        <div id="main-image" class="d-flex flex-column justify-content-center col-4 text-center">
            <i class="my-3 fa-solid fa-quote-left"></i>
            <div v-for="(comment, index) in journalSlider" :key="index">
                <div v-if="index === currentIndex">
                    <h5>{{ comment.textComment }}</h5>
                    <span class="sub-title fw-bold">{{ comment.source }}</span>
                </div>
            </div>
        </div>

        <div id="btn-next" class="col-2 d-flex justify-content-end align-items-center">
            <div class="next-position rounded-circle">
                <button @click="nextPage()" class="next btn">{{ navPage[0].next }}</button>
            </div>
        </div>
    </section>

    <div class="contain-points-slider">
        <div v-for="(comment, index) in journalSlider" :key="index">
            <div @click="isActive(index)" :class="{ 'active-point' : index === currentIndex }" class="point-slider"></div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "Slider",

    props: ["navPage", "journalSlider"],

    data() {
        return {
            currentIndex: 0,
        }
    },

    methods: {
        prevPage() {
            this.currentIndex -= 1;
            if(this.currentIndex < 0) {
                return this.currentIndex = 2;
            }
        },

        nextPage() {
            this.currentIndex += 1;
            if(this.currentIndex > 2) {
                return this.currentIndex = 0;
            }
        },

        isActive(index) {
            this.currentIndex = index;
        }
    }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

/* Utils */

.btn {
    text-decoration: $decoration-none;
    font-size: $size-small;
    color: $color-orange;
    font-weight: bold;
}

/* Slider */

#slider {
    background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
    background-position: center;
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
            right: -100px;
            transform: rotate(270deg);
            padding: 40px;
            padding-bottom: 50px;
            background-color: $color-white;
            .next {
                position: relative;
                bottom: 35px;
            }
        }
    }
    
    #content {
        height: 500px;
    }

    #main-image {
        margin: 0 auto;
        h5 {
            overflow: hidden;
        }
        i {
            font-size: 100px;
            color: rgb(183,144,60);
        }
        .sub-title {
            color: $color-orange;
            font-size: $size-small;
        }
    }

    .contain-points-slider {
        position: relative;
        display: flex;
        left: 50%;
        transform: translate(-30px);
        bottom: 100px;
        cursor: pointer;
    }

    .active-point {
        background-color: $color-dark-yellow;
    }

}

.point-slider {
    display: inline-block;
    height: 10px;
    width: 10px;
    margin-right: 10px;
    border-radius: 50%;
    background-color: $color-grey;
}

</style>