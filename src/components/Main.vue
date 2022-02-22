<template>
    <section>
      <!-- Section-Images -->
      <SectionImages :images="images" />

      <!-- Section Rating Journal -->
      <Slider :navPage="navPage" :journalSlider="journalSlider"/>

      <!-- Section Special -->
      <Special :specialSection="specialSection"/>

      <!-- Section Advertising-->
      <Advertising :advertisingSection="advertisingSection"/>

      <!-- Section Testionial -->
      <Testimonial :images="imagesTestimonial"/>

      <!-- Section Sponsor -->
      <Sponsor :images="imagesSponsors"/>

      <!-- Section Pizzas -->
      <Pizzas :pizzasSection="pizzasSection"/>

      <!-- Section Events -->
      <Events :events="eventsSection"/>

      <!-- Section Booking -->
      <Booking />

  </section>
</template>

<script>
import SectionImages from "./SectionImages.vue"
import Advertising from './Advertising.vue'
import Slider from "./Slider.vue"
import Special from "./Special.vue"
import Testimonial from "./Testimonial.vue"
import Sponsor from "./Sponsors.vue"
import Pizzas from "./Pizzas.vue" 
import Events from "./Events.vue"
import Booking from "./Booking.vue"

export default {
    name: "Main",

    components: {
        SectionImages,
        Slider,
        Special,
        Advertising,
        Testimonial,
        Sponsor,
        Pizzas,
        Events,
        Booking,
    },

    props: ["navPage"],

    data() {
        return {
            
            /* Data Images */
            images: ["1", "2", "3", "4"],

            imagesTestimonial: ["1", "2", "4", "3"],

            imagesSponsors: ["1", "2", "3", "4", "5"],

            /* Data Components */
            journalSlider: [
                {
                textComment: '"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"',
                source: "WASHINGTON POST 2018"                
                },
                {
                textComment: '"EVERY BITE IS AN EXPLOSION OF FLAVORS, DEFINITELY ONE OF THE BEST PIZZAS EVER TRIED"',
                source: "USA TODAY 2020"                
                },
                {
                textComment: '"WOAH, ARE THE ONLY WORDS YOU WILL BE ABLE TO SAY AFTER TRYING IT"',
                source: "NEW YORK, NEW YORK 2021"                
                },
            ],

            specialSection :[{
                image: "h1-img-7n.png",
                title: "SPECIALS*",
                price: ["", "$10", "$20", "$30"],
                subTitle: "COMBO",
                size: ["", "PICCOLO", "MEZZO", "GRANDE"],
                text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui."
            }],

            advertisingSection: [{
                text: "GO AHEAD AND BUILD YOUR OWN PIZZA WE WON'T JUDGE!"
            }],

            pizzasSection: [{
                choose: "CHOOSE YOUR FLAVOR",
                title: "THE BEST PIZZA MENU IN TOWN",
                text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut aliquam dui."
            }],

            eventsSection: [{
                dayDate: ["02", "03", "05"],
                monthDate: "NOV",
                typeEvents: ["TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO", "TERAZZA PATIO DINING SPACE OPENING THIS WEEKEND", "SIENNA PRIVATE DINING ROOM WITH STEPHANE BRUNN"],
                place: "204 E. Pizzetta Tommaso"
            }]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

    #section-images {

        position: relative;
        overflow: hidden;

        img {
            height: 260px;
            opacity: 1; 
            position: relative;
            z-index: 3;
            transition: opacity 1s linear;
        }

        img:hover {
            opacity: 0;
            transition: opacity 1s linear;
        }

        .eyes {
            position: absolute;
            z-index: 2;
            height: 262px;
            width: 376px;
            top: 50%;
            left: 50%;
            transform: translate(-48%, -50%);
            background-color: $color-white;

            i {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                padding: 20px;
                background-color: $color-orange;
                color: $color-white;
            }
        }
    }

</style>