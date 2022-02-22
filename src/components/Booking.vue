<template>
  <section>
      <div id="booking" class="d-flex justify-content-center align-items-center">
          <div>
            <input type="number" class="ps-3">
            <span class="px-3 fw-bold">FOR</span>
            <input type="date" class="px-3">
            <span class="px-3 fw-bold">AT</span>
            <input type="time" class="px-3">
            <button class="mx-5 fw-bold">BOOK A TABLE</button>
            <div>
                <span>*Powered by OpenTable</span>
            </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "Booking",
}
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';

#booking {
    background-image: url("../assets/img/h3-background-img-3.jpg");
    height: 300px;
    background-size: cover;
    background-position: 80%;
    background-repeat: no-repeat;

    input {
        height: 50px;
    }

    button {
        height: 50px;
        width: 200px;
        font-size: $size-small;
        background-color: $color-orange;
        color: $color-white;
        border: 0;
    }

    span {
        color: $color-white;
    }
}
</style>