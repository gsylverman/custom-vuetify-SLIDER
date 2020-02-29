<template>
  <div>
    app <modal :some="'AAAA'"></modal>
    <price-slider></price-slider>
   
  </div>
</template>

<script>
import PriceSlider from "@/components/PriceSlider/PriceSlider";
import Modal from "@/components/Modal/Modal";
export default {
  components: {
    PriceSlider,
    Modal
  },
  data() {
    return {};
  }
};
</script>
