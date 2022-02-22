<template>
  <section>
    <div class="d-flex row">
        <div id="section-images" class="col-3 my-2" v-for="(image, index) in images" :key="index">
            <img :src="require (`../assets/img/h3-img-${image}.jpg`)" alt="">
            <div class="eyes">
                <i class="rounded-circle fa-solid fa-eye"></i>
            </div>
        </div>
    </div> 
  </section>
</template>

<script>
export default {
    name: "SectionImages",

    props: ["images"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#section-images {

    position: relative;
    overflow: hidden;

    img {
        height: 260px;
        opacity: 1; 
        position: relative;
        z-index: 3;
        transition: opacity 1s linear;
    }

    img:hover {
        opacity: 0;
        transition: opacity 1s linear;
    }

    .eyes {
        position: absolute;
        z-index: 2;
        height: 262px;
        width: 376px;
        top: 50%;
        left: 50%;
        transform: translate(-48%, -50%);
        background-color: $color-white;

        i {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            padding: 20px;
            background-color: $color-orange;
            color: $color-white;
        }
    }
}
</style>