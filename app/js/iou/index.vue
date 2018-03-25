<template lang="html">
  <div>
    <Heador/>
    <Islider/>
    <Welfare/>
    <Events/>
    <Service/>
    <Rslider/>
    <Footor/>
    <Navbar/>
  </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Islider from "./islider.vue"
import Welfare from "./welfare.vue"
import Events from "./event.vue"
import Service from "./service.vue"

import Rslider  from "./rslider.vue"
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Islider,
    Welfare,
    Events,
    Service,
    Rslider
  }
}
</script>

<style lang="css">
</style>
