<template>
  <div class="createCarComp">
    <form @submit.prevent="createCar()">
      <div class="form-group">
        <label for="make">Make</label>
        <input
          type="text"
          name="make"
          class="form-control"
          placeholder="Enter make...."
          v-model="newCar.make"
        />
      </div>
      <div class="form-group">
        <label for="model">Model</label>
        <input
          type="text"
          name="model"
          class="form-control"
          placeholder="Enter model...."
          v-model="newCar.model"
        />
      </div>
      <div class="form-group">
        <label for="year">Year</label>
        <input
          type="number"
          name="year"
          class="form-control"
          placeholder="Enter year...."
          v-model="newCar.year"
        />
      </div>
      <div class="form-group">
        <label for="price">Price</label>
        <input
          type="number"
          name="price"
          class="form-control"
          placeholder="Enter price...."
          v-model="newCar.price"
        />
      </div>
      <div class="form-group">
        <label for="imgUrl">Image</label>
        <input
          type="text"
          name="imgUrl"
          class="form-control"
          placeholder="Enter imgUrl...."
          v-model="newCar.imgUrl"
        />
      </div>
      <div class="form-group">
        <label for="body">Description</label>
        <textarea
          name="body"
          class="form-control"
          placeholder="Enter body...."
          v-model="newCar.body"
        />
      </div>
      <button type="submit" class="btn btn-primary">Add Car</button>
    </form>
  </div>
</template>


<script>
export default {
  name: "createCarComp",
  data() {
    return {
      newCar: {}
    };
  },
  computed: {},
  methods: {
    createCar() {
      this.newCar.year = +this.newCar.year;
      this.newCar.price = +this.newCar.price;
      this.$store.dispatch("createCar", this.newCar);
    }
  },
  components: {}
};
</script>


<style scoped>
</style>