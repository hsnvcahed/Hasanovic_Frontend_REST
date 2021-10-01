<template>
  <div>
    {{ filteredData }}
  </div>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
    },
    cars: {
      type: Array,
    },
  },
  data() {
    return {
      filteredData: this.cars.find((el) => el.id == this.id),
    };
  },
};
</script>

<style lang="scss" scoped></style>
