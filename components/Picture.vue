<template>
  <v-row align="center" justify="center">
    <v-img
      :src="mainImage"
      :lazy-src="mainImage"
      aspect-ratio="1"
      class="grey lighten-2"
      max-width="500"
      max-height="300"
    >
      <template v-slot:placeholder>
        <v-row class="fill-height ma-0" align="center" justify="center">
          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
        </v-row>
      </template>
    </v-img>
  </v-row>
</template>

<script>
export default {
  props: {
    product: { type: Object, required: false }
  },
  data() {
    return {
      mainImage: this.product.img,
      isActive:true
    };
  },
  watch: {
    product: {
      deep: true,
      handler(val) {
        console.log(val);
        this.mainImage = val.img;
      }
    }
  }
};
</script>