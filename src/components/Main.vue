<template>
    <section>
      <section>

        <div class="d-flex row">
            <div id="section-images" class="col-3 my-2" v-for="(image, index) in images" :key="index">
                <img :src="require (`../assets/img/h3-img-${image}.jpg`)" alt="">
            </div>
        </div> 
      </section>

      <!-- Section Rating Journal -->
      <Slider :navPage="navPage" :journalSlider="journalSlider"/>

      <!-- Section Special -->
      <Special :specialSection="specialSection"/>

      <!-- Section Advertising-->
      <Advertising :advertisingSection="advertisingSection"/>

      <!-- Section Testionial -->
      <Testimonial :images="imagesTestimonial"/>

  </section>
</template>

<script>
import Advertising from './Advertising.vue'
import Slider from "./Slider.vue"
import Special from "./Special.vue"
import Testimonial from "./Testimonial.vue"

export default {
    name: "Main",

    components: {
        Slider,
        Special,
        Advertising,
        Testimonial,
    },

    props: ["navPage"],

    data() {
        return {
            
            images: ["1", "2", "3", "4"],

            imagesTestimonial: ["1", "2", "4", "3"],

            journalSlider: [{
                textComment: "FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES",
                source: "WASHINGTON POST 2018"                
            }],

            specialSection :[{
                image: "h1-img-7n.png",
                title: "SPECIALS*",
                price: ["", "$10", "$20", "$30"],
                subTitle: "COMBO",
                size: ["", "PICCOLO", "MEZZO", "GRANDE"],
                text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui."
            }],

            advertisingSection: [{
                text: "GO AHEAD AND BUILD YOUR OWN PIZZA WE WON'T JUDGE"
            }],
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