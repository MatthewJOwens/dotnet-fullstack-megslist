<template>
  <div class="carListComp col-3 m-3 border rounded">
    <h1>{{carData.make}}</h1>
    <h2>{{carData.model}}</h2>
    <img :src="carData.imgUrl" class="img-fluid" alt srcset />
    <h2>{{carData.price}}</h2>
    <h2>{{carData.year}}</h2>
    <h2>{{carData.body}}</h2>
    <button class="btn btn-danger btn-block" @click="deleteCar(carData.id)">Delete</button>
  </div>
</template>


<script>
export default {
  name: "carListComp",
  props: ["carData"],
  data() {
    return {};
  },
  computed: {},
  methods: {
    deleteCar(carId) {
      this.$store.dispatch("deleteCar", carId);
    }
  },
  components: {}
};
</script>


<style scoped>
</style>