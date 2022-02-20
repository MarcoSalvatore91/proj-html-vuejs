<template>
  <section id="slider" class="my-2">
    <section id="content" class="row justify-content-between">
        <div class="col-2 d-flex align-items-center">
            <a href="#">{{ navPage[0].prev }}</a>
        </div>

        <div id="main-image" class="d-flex flex-column justify-content-center col-4 text-center" v-for="content in journalSlider" :key="content.id">
            <p>{{ content.textComment }}</p>
            <span>{{ content.source }}</span>
        </div>

        <div class="col-2 d-flex justify-content-end align-items-center">
            <a href="#">{{ navPage[0].next }}</a>
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

#slider {
    background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
    background-position: center;
}

#content {
    height: 400px;
}

#main-image {
    margin: 0 auto;
}

</style>