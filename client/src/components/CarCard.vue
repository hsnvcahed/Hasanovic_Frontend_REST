<template>
  <v-card class="d-flex flex-column">
    <v-img :src="carData.image"></v-img>

    <v-card-title>
      {{ carData.title }}
    </v-card-title>

    <v-card-subtitle>
      Owner:
      <span class="font-weight-bold">
        {{ carData.owner.firstName }}
        {{ carData.owner.lastName }}
      </span>
    </v-card-subtitle>
    <v-card-subtitle>
      Year: <span class="font-weight-bold">{{ carData.yearOfMake }}</span>
    </v-card-subtitle>
    <v-card-subtitle>
      Miles:<span class="font-weight-bold"> {{ carData.miles }}</span>
    </v-card-subtitle>
    <v-card-subtitle>
      Price:<span class="font-weight-bold"> {{ carData.price }}</span>
    </v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange lighten-2" text>
        Explore
      </v-btn>

      <v-spacer></v-spacer>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    carData: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" scoped></style>
