<template>
  <section>
      <div class="bg-sand">
        <div id="sponsors" class="d-flex">
            <div class="mb-2" v-for="image in images" :key="image">
                <img :src="require (`../assets/img/h1-clients-img-${image}.png`)" alt="">
            </div>
        </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "Sponsor",

    props: ["images"]
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

.bg-sand {
    background-color: $bgc-sand;
}

#sponsors {
    width: $width-min;
    margin: $content-center;
    padding: 100px 0;
}
</style>