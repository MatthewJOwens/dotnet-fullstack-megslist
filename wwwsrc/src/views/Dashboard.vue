<template>
  <div class="dashboard">
    <h1>WELCOME TO THE DASHBOARD</h1>
    <cars />
    <!-- <cars v-show="showCars">Cars Component template not loaded.</cars> -->
    <!-- <houses v-show="showHouses"></houses> -->
  </div>
</template>

<script>
import Cars from "../components/Cars.vue";
// import Houses from "../components/Houses.vue";
export default {
  data() {
    return {
      showCars: true,
      showHouses: false
    };
  },
  mounted() {},
  computed: {},
  components: {
    Cars
  }
};
</script>

<style></style>
