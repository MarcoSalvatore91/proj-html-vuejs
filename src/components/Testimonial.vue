<template>
  <section>
        <div class="d-flex">
            <div class="mb-2" v-for="image in images" :key="image">
                <img :src="require (`../assets/img/h1-team-${image}a.jpg`)" alt="">
            </div>
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

img {
    height: 400px;
    width: 400px;
}
</style>