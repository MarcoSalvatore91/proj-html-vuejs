<template>
  <section>
      <div id="add" class="row align-items-center my-2" v-for="advertising in advertisingSection" :key="advertising.id">
          <h1 class="col-3 offset-3">{{ advertising.text }}</h1>
      </div>
  </section>
</template>

<script>
export default {
    name: "Advertising",

    props: ["advertisingSection"]
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#add {
    background-image: url(../assets/img/h3-background-img.jpg);
    height: 600px;
    background-position: center;
    background-repeat: no-repeat;

    h1 {
        overflow: hidden;
        color: $color-white;
        font-size: 60px;
    }
}

</style>