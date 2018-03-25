<template lang="html">
  <Panel :class="$style.panel">
    <section :class="$style.content">
      <swiper :options="options">
        <swiper-slide>百万白条券免费送，速来领取！<em>></em></swiper-slide>
        <swiper-slide>签到领流量，1元500兆<em>></em></swiper-slide>
      </swiper>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
import {swiper, swiperSlide} from 'vue-awesome-swiper';
export default {
  components: {
    Panel,
    swiper,
    swiperSlide,
  },
  data() {
    return {
      options: {
        autoplay: true,
        loop: true,
        direction: "vertical"
      }
    }
  }
}
</script>
<style lang="scss">
  // @import "~swiper/dist/css/swiper.css";
  .swiper-container-vertical {
    height: 72px;
    .swiper-slide {
      font-family: PingFangSC-Medium;
      color: #333;
      font-size: 28px;
      em {
        color: #ddd;
        float: right;
        margin-right: 20px;
      }
    }
  }
</style>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  >h4 {
    display: none;
  }
  .content {
    height: 72px;
    line-height: 72px;
    overflow: hidden;
    background: url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) no-repeat left center;
    padding-left: 140px;
  }
}
</style>
