<template>
  <section id="special">
      <div class="row" v-for="special in specialSection" :key="special.id">
        <div id="bg-side" class="col-6">
            <img :src="require (`../assets/img/${special.image}`)" alt="">
        </div>

        <div class="row section-combo col-6 align-items-center">

            <div class="col-7 offset-3">
                <div>
                    <h1>{{ special.title }}</h1> 
                    <p>{{ special.text }}</p>   
                </div>

                <div v-for="i in 3" :key="i">
                    <div class="d-flex">
                        <h3>{{ special.price[i] }}</h3>
                        <h3>{{ special.subTitle }}</h3>
                        <h3>{{ special.size[i] }}</h3>
                    </div>
                    <p>{{ special.text }}</p>
                </div>
            </div>

        </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "Special",

    props: ["specialSection"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#bg-side {
    height: 800px;
    background-image: url(../assets/img/h1-img-4.jpg);

    img {
        height: 400px;
        position: relative;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}

.section-combo {

    h1, h3 {
        overflow: hidden;
        padding-right: 10px;
    }
}


</style>