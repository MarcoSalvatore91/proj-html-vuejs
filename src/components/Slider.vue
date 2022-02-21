<template>
  <section id="slider" class="my-2">
    <section id="content" class="row justify-content-between">
        <div id="btn-prev" class="col-2 d-flex align-items-center">
            <div class="prev-position rounded-circle">
                <a href="#" class="prev">{{ navPage[0].prev }}</a>
            </div>
        </div>

        <div id="main-image" class="d-flex flex-column justify-content-center col-4 text-center" v-for="content in journalSlider" :key="content.id">
            <i class="my-3 fa-solid fa-quote-left"></i>
            <h5>{{ content.textComment }}</h5>
            <span class="sub-title fw-bold">{{ content.source }}</span>
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
    name: "Slider",

    props: ["navPage", "journalSlider"]
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

/* Slider */

#slider {
    background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
    background-position: center;
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

</style>