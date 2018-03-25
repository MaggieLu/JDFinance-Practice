<template lang="html">
  <Panel :class="$style.panel">
    <section :class="$style.content">
      <Slider :cname="$style.slider" :items="items"></Slider>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
  components: {
    Panel,
    Slider,
  },
  data() {
    return {
      items: [{
        href: "iou",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t16798/322/621991060/49914/ec0d539b/5a991ebcN932c6731.jpg?width=750&height=320"
      }]
    }
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  .content {
    .slider {
      img{
        width: 100%;
      }
    }
  }
}
</style>
