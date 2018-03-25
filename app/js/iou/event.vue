<template lang="html">
  <Panel title="精品活动" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item" v-for="item in items" :key="item.name">
        <img :src="item.src" alt="">
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
  components: {
    Panel,
  },
  data() {
    return {
      items: [{
        name: "ad1",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t17374/350/576442826/54240/a9918a9/5a97d2c0N021cf2e0.png?width=376&height=264"
      }, {
        name: "ad2",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t14653/159/1840910093/27778/53ebfb91/5a5c5cc9N28e0dc96.png?width=376&height=264"
      }]
    }
  }
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel {
    @include panel;
    padding-bottom: 20px;
    .content {
      @include flex(row);
      justify-content: space-around;
      .item {
        width: 50%;
        img {
          width: 100%;
        }
      }
    }
  }
</style>
