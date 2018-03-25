<template lang="html">
  <section :class="cname">
    <swiper :options="options" :not-next-tick="options.notNextTick">
      <!-- -- we dont know how many photos we have, so user slot
      or array, slot cannot be used here, because we have to use
      swiper-slide, then we need to import awesomeslider eerywhere.
      so use array-->
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link :to="{name: item.href}">
          <img :src="item.src">
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination" v-if="options.pagination"></div>
    </swiper>
  </section>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper';
export default {
  components: {
    swiper,
    swiperSlide, // 这样注册完就可以使用
  },
  props: {
    cname: {
      type: String,
      default: ""
    },
    options: {
      type: Object, // default of Object must be returned,-- it's the rule
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: '.swiper-pagination',
          },
          notNextTick: false,
        }
      }
    },
    items: {
      type: Array,
      default() {
        return [] // [{href:'', src:''}]
      }
    }
  },
}
</script>

<style lang="scss">
  @import "~swiper/dist/css/swiper.css";
</style>
