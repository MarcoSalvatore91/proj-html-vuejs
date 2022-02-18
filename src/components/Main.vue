<template>
  <section>
      <section>
        <div v-for="(image, index) in item" :key="index">
            <Card :format="format" :item="item[index]" :type="type"/>
        </div>
        <!-- <div class="d-flex row">
            <div class="col-3 my-2" v-for="(image, index) in images" :key="index">
                <img :src="require (`../assets/img/h3-img-${image}.jpg`)" alt="">
            </div>
        </div> -->
      </section>
  </section>
</template>

<script>
import Card from "./Card.vue"

export default {
    name: "Main",

    components: {
        Card,
    },

    data() {
        return {
            format: "../assets/img/h3-img-",
            item: ["1", "2", "3", "4"],
            type: "jpg",
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