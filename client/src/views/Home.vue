<template>
  <v-container>
    <LogoBar />
    <CarCards style="width:100%" :cars="cars" />
  </v-container>
</template>

<script>
import LogoBar from '@/components/LogoBar.vue';
import CarCards from '@/components/CarCards.vue';
export default {
  name: 'Home',
  props: {
    cars: {
      type: Array,
    },
  },
  components: {
    LogoBar,
    CarCards,
  },
};
</script>
