<script>
import Img1 from '@/assets/images/1-ad.png';
import Img2 from '@/assets/images/2-ad.png';
import Img3 from '@/assets/images/3-ad.png';

export default {
  props: ['adNumber'],
  computed: {
    img() {
      if (this.adNumber === 1) {
        return Img1;
      } else if (this.adNumber === 2) {
        return Img2;
      } else if (this.adNumber === 3) {
        return Img3;
      } return '';
    },
  },
};
</script>
<template src="./Ad.html"></template>
<style lang="scss" src="./Ad.scss"></style>
