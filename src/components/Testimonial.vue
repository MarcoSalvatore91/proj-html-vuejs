<template>
  <section>
        <div class="d-flex">
            <div class="mb-2" v-for="image in images" :key="image">
                <img class="img-people" :src="require (`../assets/img/h1-team-${image}a.jpg`)" alt="">
            </div>
        </div>
        <div>
          <img class="svg rounded-circle" src="../assets/svg/svg-4.svg" alt="slice-pizza">
        </div>
  </section>
</template>

<script>
export default {
    name: "Testimonial",

    props: ["images"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

section {
    position: relative;

    .img-people {
        height: 400px;
        width: 400px;
    }

    .svg {
        position: absolute;
        padding: 20px;
        background-color: rgb(246,247,242);
        bottom: 30px;
        right: 50px;
    }
}

</style>