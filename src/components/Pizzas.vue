<template>
  <section>

      <!-- Title -->
      <div id="title" class="text-center" v-for="pizza in pizzasSection" :key="pizza.id">
          <span>{{ pizza.choose }}</span>
          <h1>{{ pizza.title }}</h1>
          <p>{{ pizza.text }}</p>
      </div>

      <!-- Pizza -->
      <div id="pizza" class="d-flex justify-content-between">
          <div class="pizza-start">
              <img src="../assets/img/h3-product-img-1a-100x100.png" alt="Bismark">
              <div class="pizza-type">
                <span>BISMARK</span>
                <div class="d-flex justify-content-center">
                    <span class="text-decoration-line-through pe-2">$5.00</span><span>$30.00</span>
                </div>
              </div>
          </div>
          <div id="pizza-middle" class="d-flex justify-content-between mb-5">
            <div>
                <img src="../assets/img/h3-product-img-2a-150x150.png" alt="Fiori di zucca">
                <div class="pizza-type">
                    <span>FIORI DI ZUCCA</span>
                    <span>$7.00 - $50.00</span>
                </div>
            </div>
            <div class="rel-position">
                <img src="../assets/img/h3-product-img-3a-150x150.png" alt="Valdostana">
                <span class="sold rounded-circle fw-bold">SOLD</span>
                <div class="pizza-type">
                    <span>VALDOSTANA</span>
                    <span>$55.00</span>
                </div>
            </div>
            <div>
                <img src="../assets/img/h3-product-img-4a-150x150.png" alt="Pizza Tartufata">
                <div class="pizza-type">
                    <span>PIZZA TARTUFATA</span>
                    <span>$45.00</span>
                </div>
            </div>
            <div>
                <img src="../assets/img/h3-product-img-5a-150x150.png" alt="Francescana">
                <div class="pizza-type">
                    <span>FRANCESCANA</span>
                    <span>$25.00</span>
                </div>
            </div>
          </div>
          <div class="pizza-end">
              <img src="../assets/img/h3-product-img-6a-100x100.png" alt="Campagnola">
              <div class="pizza-type">
                <span>CAMPAGNOLA</span>
                <span>$50.00 - $95.00</span>
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
    }
    
    img {
        height: 200px;
    }

    span {
        display: block;
        text-align: center;
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