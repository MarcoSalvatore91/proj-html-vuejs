<template>
  <section>
      <div id="events" class="row mt-5 mb-2">
        <div class="row col-6 data d-flex align-items-center">
            <div class="col-8 offset-2">
                <div id="section-title">
                    <span class="top-title fw-bold">MADE WITH LOVE</span>
                    <h2 class="title">DELISH PIZZA DEALS</h2>
                </div>
                
                <div class="place-event d-flex" v-for="event in events" :key="event.id">
                    <div class="pe-5">
                        <span class="day-date fw-bold">{{ event.dayDate[0] }}</span><br>
                        <span class="month-date fw-bold">{{ event.monthDate }}</span>
                    </div>
                    <div class="d-flex flex-column justify-content-center type-event">
                        <h4>{{ event.typeEvents[0] }}</h4>
                        <span>{{ event.place }}</span>
                    </div>
                </div>
                <hr>

                <div class="place-event d-flex" v-for="event in events" :key="event.id">
                    <div class="pe-5">
                        <span class="day-date fw-bold">{{ event.dayDate[1] }}</span><br>
                        <span class="month-date fw-bold">{{ event.monthDate }}</span>
                    </div>
                    <div class="d-flex flex-column justify-content-center type-event">
                        <h4>{{ event.typeEvents[1] }}</h4>
                        <span>{{ event.place }}</span>
                    </div>
                </div>
                <hr>

                <div class="place-event d-flex" v-for="event in events" :key="event.id">
                    <div class="pe-5">
                        <span class="day-date fw-bold">{{ event.dayDate[2] }}</span><br>
                        <span class="month-date fw-bold">{{ event.monthDate }}</span>
                    </div>
                    <div class="d-flex flex-column justify-content-center type-event">
                        <h4>{{ event.typeEvents[2] }}</h4>
                        <span>{{ event.place }}</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="bgc-image col-6"></div>
      </div>
  </section>
</template>

<script>
export default {
    name: "event",

    props: ["events"],
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#events {
    height: 900px;

    .data {

        background-color: $bgc-black;
        height: 800px;

        #section-title {
            padding-bottom: 30px;

            .top-title {
                color: $color-orange;
                font-size: $size-small;
            }

            .title {
                overflow: hidden;
                color: $color-white;
            }
        }
    }

    .place-event {

        
        .day-date {
            font-size: 40px;
            color: $color-orange;
            }
        
        .month-date {
            font-size: 25px;
            color: $color-white;
        }

        .type-event {

            h4 {
                overflow: hidden;
                color: $color-white;
            }

            span {
                color: $color-orange;
            }
        }

    }

    .bgc-image {
        background-image: url("../assets/img/h3-img-5a.jpg");
    }

    hr {
        margin: 40px 0;
        border-top: 3px dotted yellow;
    }
}

</style>