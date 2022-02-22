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
                    <p class="fw-bold">{{ special.text }}</p>   
                </div>

                <div v-for="i in 3" :key="i">
                    <div class="d-flex">
                        <h3 class="price">{{ special.price[i] }}</h3>
                        <h3>{{ special.subTitle }}</h3>
                        <h3>{{ special.size[i] }}</h3>
                    </div>
                    <p class="text-combo fw-bold">{{ special.text }}</p>
                </div>
            </div>

        </div>
      </div>

      <div>
          <img class="svg rounded-circle" src="../assets/svg/svg-4.svg" alt="slice-pizza">
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

/* Utils */

p {
    color: $color-grey;
}

/* Special */

#special {
    position: relative;

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
    
        .price {
            color: $color-orange;
        }
    
        h1, h3 {
            overflow: hidden;
            padding-right: 10px;
        }
    
        .text-combo {
            padding-left: 55px;
            font-size: $size-small;
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