<template lang="html">
  <section :class="[panelClass, cname]">
    <h4>-{{ title }}-</h4>
    <slot/>
  </section>
  </div>
  </div>
</template>

<script>
export default {
  props: {
    cname: {
      type: String,
      defaule: "",
    },
    title: {
      type: String,
      default: "",
    }
  },
  data() {
    return {
      panelClass: "panel",
    }
  }
}
</script>

<style lang="scss">
@import "../../css/element.scss";
.panel {
  @include panel;
}
</style>
