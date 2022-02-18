<template>
  <section>
      <section>
        <div class="d-flex row">
            <div class="col-3 my-2" v-for="(image, index) in images" :key="index">
                <img :src="require (`../assets/img/h3-img-${image}.jpg`)" alt="">
            </div>
        </div>
      </section>
  </section>
</template>

<script>
export default {
    name: "Main",

    data() {
        return {
            images: ["1", "2", "3", "4"]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';
    img {
        height: 260px;
    }
</style>