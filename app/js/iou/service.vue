<template lang="html">
  <Panel title="更多服务" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item" v-for="item in items" :key="item.title">
        <router-link :to="{ name: 'iou'}">
          <img :src="item.src" alt="">
          <p>{{ item.title }}</p>
        </router-link>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
  components: {
    Panel,
  },
  data() {
    return {
      items: [{
        title: "小白卡",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t4609/245/3975151339/11019/766e751d/590aca78Nf15a7947.png?width=135&height=135"
      },{
        title: "白条商城",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t5269/224/1031852465/12646/40e0f799/590aca55N22a6f274.png?width=135&height=135"
      },{
        title: "消费分期",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t5095/216/1045040184/12370/564ae632/590ac7deN9a0eac2a.png?width=135&height=135"
      },{
        title: "借钱",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t8311/300/1385281399/9501/130a0046/59b8da06N14f62cf3.png?width=120&height=120"
      },{
        title: "白条提额",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135"
      },{
        title: "白条闪付",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t4417/98/4154366136/13785/5433ca92/590ac8afN5dd91d6e.png?width=135&height=135"
      },{
        title: "小白会玩",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t4453/75/4132459214/14188/939b7f34/590ac860N752d5738.png?width=135&height=135"
      },{
        title: "钢镚",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t5371/323/1038197138/12031/3ec72f6c/590aca20N089fd34a.png?width=135&height=135"
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
    @include flex(row);
    justify-content: space-around;
    .item {
      width: 160px;
      text-align: center;
      padding-bottom: 40px;
      a {
        font-size: 26px;
        color: #666;
        text-decoration: none;
      }
      img {
        width: 90px;
        height: 90px;
      }
      p {
        margin-top: 12px;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
      }
    }
  }
}
</style>
