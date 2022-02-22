<template>
  <section>
      <div id="add" class="row align-items-center my-2" v-for="advertising in advertisingSection" :key="advertising.id">
          <h1 class="col-3 offset-3">{{ advertising.text }}</h1>
      </div>
      <div>
          <img class="svg rounded-circle" src="../assets/svg/svg-4.svg" alt="slice-pizza">
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

section {
    position: relative;

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

    .svg {
        position: absolute;
        padding: 20px;
        background-color: rgb(246,247,242);
        bottom: 250px;
        right: 50px;
    }
}


</style>