<template lang="html">
  <Panel title="精选推荐" :class="$style.panel">
    <section :class="$style.content">
      <dl :class="$style.item" v-for="item in items" :key="item.title">
        <dt>{{ item.title }}<span>{{ item.sub }}</span></dt>
        <dd>{{ item.rate }}</dd>
        <dd>{{ item.text }}</dd>
      </dl>
  </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
  components: {
    Panel
  },
  data() {
    return {
      items: [{
        title: "定期理财",
        sub: "90天可质押",
        rate: "5.50%",
        text: "历史年化结算利率"
      },{
        title: "固收理财",
        sub: "理财推荐",
        rate: "5.80%",
        text: "综合年化收益率"
      },{
        title: "基智账户",
        sub: "组合投资",
        rate: "8%-10%",
        text: "止盈年化收益率"
      },{
        title: "小白基金",
        sub: "超短期",
        rate: "5.00%",
        text: "7日年化收益率"
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
    &:after {
      content: " ";
      width: 100%;
      border-bottom: 1px solid #eee;
      position: relative;
      top: -208px;
    }
    .item {
      width: 50%;
      padding: 34px 16px;
      box-sizing: border-box;
      position: relative;
      &:after {
        content: " ";
        width: 0;
        height: 136px;
        border-right: 1px solid #eee;
        position: absolute;
        top: 50%;
        right: 0;
        margin-top: -68px;
      }
      &:nth-child(2n):after {
        display: none;
      }
      dt {
        color: #333;
        font-weight: 700;
        font-size: 30px;
        height: 42px;
        line-height: 42px;
        span {
          font-size: 22px;
          padding: 0 8px;
          color: #FF5155;
          text-align: center;
          vertical-align: 1px;
          margin-left: 4px;
          border: 1px solid #FF5155;
        }
      }
      dd {
        &:nth-child(2) {
          font-size: 44px;
          font-weight: 700;
          height: 58px;
          line-height: 58px;
          color: #FF5155;
          white-space: nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
        }
        &:nth-child(3) {
          font-size: 24px;
          height: 34px;
          line-height: 34px;
          color: #999;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
      }
    }
  }
}
</style>
