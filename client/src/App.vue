<template>
  <v-app>
    <v-main>
      <router-view :cars="cars" />
    </v-main>
  </v-app>
</template>

<script>
import axios from 'axios';

export default {
  name: 'App',

  data: () => ({
    //
    cars: [],
  }),
  methods: {
    async getCars() {
      let result = await axios({
        url: 'http://localhost:3000/cars',
        method: 'GET',
      });

      console.log(result);
      this.cars = result.data;
    },
  },
  created() {
    this.getCars();
  },
};
</script>
