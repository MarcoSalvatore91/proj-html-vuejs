<template>
  <section>
    <div class="d-flex row">
        <div class="col-3 my-2">
            <img :src="require (`${format}${item}.${type}`)" alt="">
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "Card",

    props: ["format", "item", "type"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

</style>