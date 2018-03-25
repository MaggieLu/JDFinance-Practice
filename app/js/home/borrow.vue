<template lang="html">
  <Panel title="极速借贷" :class="$style.panel">
    <section :class="$style.content">
      <router-link :to="{ name: 'home'}">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16420/311/2441901775/41509/ea55e221/5aaa4d09Nffaa582e.jpg?width=750&height=320">
      </router-link>
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
.panel {
  @include panel;
  .content {
    padding-bottom: 40px;
    img {
      display: block;
      width: 100%;
    }
  }
}

</style>
