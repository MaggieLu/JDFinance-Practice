<template lang="html">
  <Panel title="下载APP" :class="$style.panel">
    <section :class="$style.content">
      <div></div>
      <p>立即下载</p>
      <span>copyright</span>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
  components: {
    Panel,
  }
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  html, body {
    background: #fff;
  }
  .panel {
    @include panel;
    margin: 0;
    h4 {
      display: none;
    }
    .content {
      @include flex;
      justify-content: center;
      align-items: center;
      height: 1136px;
      width: 100%;
      >div {
        width: 600px;
        height: 640px;
        background: url(//wyyl.jd.com/static/page/images/redpacket.png) center;
        background-size: 100%;
        margin-top: -200px;
      }
      >p {
        @include btn($size: 32px);
        height: 100px;
        line-height: 100px;
        width: 470px;
        background-image: linear-gradient(270deg, #f55c33 0, #ee2d1b 75%);
        box-shadow: 0 12px 16px 0 rgba(233, 159, 135, .6);
        position: fixed;
        bottom: 130px;
      }
      span {
        position: fixed;
        bottom: 16px;
        font-size: 24px;
        color: #ddd;
      }
    }
  }
</style>
