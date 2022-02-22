<template>
    <section>
        <div class="row">
            <div id="place-restaurant" class="row col-7 d-flex">
                <div class="col-4">
                    <span class="title">FIND OUR RESTURANTS</span>
                    <div class="mt-4" v-for="place in restaurants" :key="place.id">
                        <span class="grey">{{ place.road }}</span><br>
                        <span class="grey">{{ place.place }}</span><br>
                        <span class="grey">{{ place.number }}</span>
                    </div>
                </div>
                <div class="col-4">
                    <div>
                        <span class="title">WORKING HOURS</span>
                        <div class="mt-4" v-for="day in openDays" :key="day.id">
                            <span class="title">{{ day.day }}</span><br>
                            <span :class="{ orange : day.openHour === 'Kitchen Closed', grey : day.openHour !== 'Kitchen Closed' }">{{ day.openHour }}</span>
                        </div>
                    </div>
                    <div class="mt-4">
                        <span class="title">FOLLOW US:</span>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-linkedin-in"></i>
                    </div>
                </div>
                <div class="col-4 white" v-for="text in footerText" :key="text.id">
                    <h4>{{ text.text }}</h4>
                </div>
                <div id="sign" class="d-flex flex-end">
                    <span class="yellow">Created with &hearts; by</span><span class="green ps-2">Qode Interactive</span>
                </div>
            </div>
            <div id="bg-image" class="col-5"></div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Footer",

    props: ["restaurants", "openDays", "footerText"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

section {
    height: 750px;
    background-color: $bgc-black;
}

#bg-image {
    height: 750px;
    background-image: url("../assets/img/footer-img-1.jpg");
}

#place-restaurant {
    padding: 50px;
    position: relative;
    margin-top: 100px;

    .title {
        color: $color-dark-yellow;
        font-weight: bold;
    }

    #sign {
        position: absolute;
        bottom: 20px;
        left: 60px;
    }

    i {
        color: $color-white;
        font-size: 0.7rem;
        padding: 0 2px;
    }

    h4 {
        overflow: hidden;
    }
}

/* Colors */

.orange {
    color: $color-orange;
}

.yellow {
    color: $color-dark-yellow;
}

.green {
    color: $color-green;
}

.grey {
    color: $color-grey;
}

.white {
    color: $color-white;
}
</style>