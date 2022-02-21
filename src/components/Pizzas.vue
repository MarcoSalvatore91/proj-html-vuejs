<template>
  <section>

      <!-- Title -->
      <div id="title" class="text-center" v-for="pizza in pizzasSection" :key="pizza.id">
          <span class="choose fw-bold">{{ pizza.choose }}</span>
          <h1>{{ pizza.title }}</h1>
          <p class="text-under-title">{{ pizza.text }}</p>
      </div>

      <!-- Pizza -->
      <div id="pizza" class="d-flex justify-content-between">
          <div class="pizza-start">
              <img src="../assets/img/h3-product-img-1a-100x100.png" alt="Bismark">
              <div class="pizza-type">
                <span class="text-yellow">BISMARK</span>
                <div class="d-flex justify-content-center">
                    <span class="text-decoration-line-through pe-2 text-orange">$5.00</span><span class="text-orange">$30.00</span>
                </div>
              </div>
          </div>
          <div id="pizza-middle" class="d-flex justify-content-between mb-5">
            <div>
                <img src="../assets/img/h3-product-img-2a-150x150.png" alt="Fiori di zucca">
                <div class="pizza-type">
                    <span class="text-yellow">FIORI DI ZUCCA</span>
                    <span class="text-orange">$7.00 - $50.00</span>
                </div>
            </div>
            <div class="rel-position">
                <img src="../assets/img/h3-product-img-3a-150x150.png" alt="Valdostana">
                <span class="sold rounded-circle fw-bold">SOLD</span>
                <div class="pizza-type">
                    <span class="text-yellow">VALDOSTANA</span>
                    <span class="text-orange">$55.00</span>
                </div>
            </div>
            <div>
                <img src="../assets/img/h3-product-img-4a-150x150.png" alt="Pizza Tartufata">
                <div class="pizza-type">
                    <span class="text-yellow">PIZZA TARTUFATA</span>
                    <span class="text-orange">$45.00</span>
                </div>
            </div>
            <div>
                <img src="../assets/img/h3-product-img-5a-150x150.png" alt="Francescana">
                <div class="pizza-type">
                    <span class="text-yellow">FRANCESCANA</span>
                    <span class="text-orange">$25.00</span>
                </div>
            </div>
          </div>
          <div class="pizza-end">
              <img src="../assets/img/h3-product-img-6a-100x100.png" alt="Campagnola">
              <div class="pizza-type">
                <span class="text-yellow">CAMPAGNOLA</span>
                <span class="text-orange">$50.00 - $95.00</span>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "Pizzas",

    props: ["pizzasSection"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#title {

    margin: 100px 0;

    h1 {
        overflow: hidden;
    }

    .choose {
        font-size: $size-small;
        color: $color-orange;
    }

    .text-under-title {
        font-size: $size-large;
        color: $color-grey;
    }
}

#pizza {
    .pizza-start {
        position: relative;
        right: 70px;
    }

    .pizza-end {
        position: relative;
        left: 70px;
    }

    #pizza-middle {
        width: 1070px;
    }

    .pizza-type {
        margin-top: 20px;
        .text-yellow {
            color: $color-dark-yellow;
        }
        .text-orange {
            color: $color-orange;
        }
    }
    
    img {
        height: 200px;
    }

    span {
        display: block;
        text-align: center;
        font-weight: bold;
    }

    .rel-position {
        position: relative;
        .sold {
            position: absolute;
            top: 0;
            right: 0;
            padding: 20px 13px;
            font-size: $size-medium;
            background-color: $color-orange;
        }
    }
}
</style>