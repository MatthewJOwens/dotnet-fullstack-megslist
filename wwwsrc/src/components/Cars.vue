<template>
  <div class="Cars">
    <CreateCarComp />
    <div class="row justify-content-center">
      <CarListComp v-for="car in cars" :key="car.id" :carData="car" />
    </div>
  </div>
</template>


<script>
import CarListComp from "./CarListComp";
import CreateCarComp from "./CreateCarComp";
export default {
  name: "Cars",
  data() {
    return {};
  },
  mounted() {
    this.$store.dispatch("getCars");
  },
  computed: {
    cars() {
      return this.$store.state.cars;
    }
  },
  methods: {},
  components: { CarListComp, CreateCarComp }
};
</script>


<style scoped>
</style>