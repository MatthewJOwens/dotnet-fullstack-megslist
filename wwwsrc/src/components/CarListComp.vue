<template>
  <div
    class="carListComp col-3 m-3 border rounded"
    @click="$router.push({name: 'car', params: {carId: carData.id}})"
  >
    <h1>Make: {{carData.make}}</h1>
    <h2>Model: {{carData.model}}</h2>
    <img :src="carData.imgUrl" class="img-fluid" alt srcset />
    <h2>Price: {{carData.price}}</h2>
    <h2>Year: {{carData.year}}</h2>
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
  methods: {},
  components: {}
};
</script>


<style scoped>
</style>