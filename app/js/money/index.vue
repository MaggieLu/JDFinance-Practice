<template lang="html">
  <!-- entry file -->
    <div>
        <Heador/>
        <Slider/>
        <Ada/>
        <Recommend/>
        <Adb/>
        <Choice/>
        <Footor cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from '../public/header.vue' // cannot use Header, beause its forbidden to use in Vue.
import Footor from '../public/footer.vue'
import Navbar from '../public/navbar.vue'
import Slider from './mslider.vue'
import Ada from './ada.vue'
import Recommend from './recommend.vue'
import Adb from './adb.vue'
import Choice from './choice.vue'
export default {
  components: {
    Heador,
    Slider,
    Footor,
    Navbar,
    Ada,
    Recommend,
    Adb,
    Choice
  }
}
</script>

<style lang="scss">
  .mfooter{
    margin-top: 0 !important;
    ul {
      li:first-child {
          display: none;
      }
    }
  }
</style>
