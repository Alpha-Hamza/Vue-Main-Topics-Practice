<template>
  <h1 class="heading">Watch property:</h1>
  <div id="computed_props" class="inputs">
    Kilometers : <input type="text" v-model="kilometers" /> Meters :
    <input type="text" v-model="meters" />
  </div>
</template>

<script>
export default {
  name: "watch",
  data() {
    return {

        kilometers: 0,
        meters: 0,
    }
  },
  watch: {
    kilometers: function (val) {
      this.kilometers = val;
      this.meters = val * 1000;
    },
    meters: function (val) {
      this.kilometers = val / 1000;
      this.meters = val;
    },
  },
};
</script>

<style scoped>
.heading {
  margin-top: 50px;
 text-align: center;
   
}
.inputs > input {

  color: black;
  border: 1px #41b883 solid;
  height: 30px;
  width: 150px; 
}
</style>

