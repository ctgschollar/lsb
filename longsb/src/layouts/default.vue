<template>
  <q-layout view="hhh lpr FFF">
    <q-layout-header reveal :reveal-offset="250">
      <q-btn color="primary" label="About" @click="scrollToElement('about')"/>
      <q-btn color="primary" label="Facilities" @click="scrollToElement('facilities')"/>
      <q-btn color="primary" label="Location" @click="scrollToElement('location')"/>
      <q-btn color="primary" label="Rooms" @click="scrollToElement('rooms')"/>
      <q-btn color="primary" label="Neighbours" @click="scrollToElement('neightbours')"/>
      <q-btn color="primary" label="Book" @click="scrollToElement('facilities')"/>
    </q-layout-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-layout-footer class="bg-primary">
      <form id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
        <div class="container row justify-around">
          <q-datetime inverted class="q-pa" type="date" v-model="date" name="widget_date" id="date_1"/>
          <q-datetime inverted type="date" name="widget_date_to" v-model="dateTo" id="date_2"/>
          <input type="hidden" value="d/m/Y" name="date_format">
          <q-btn class="text-white bg-primary" type="submit" name="bf_submit" label="Check Availability"/>
          <!--<div class="q-title text-white vertical-middle"> BOOK NOW </div>-->
          <div class="clear_floats"></div>
        </div>
      </form>
    </q-layout-footer>
  </q-layout>
</template>

<script>
import { date, scroll } from 'quasar'

const { getScrollTarget, setScrollPosition } = scroll

export default {
  name: 'LayoutDefault',
  data () {
    return {
      state: true,
      footer: true,
      header: true,
      date: new Date(),
      dateTo: date.addToDate(new Date(), { days: 1 })
    }
  },
  methods: {
    scrollToElement (elid) {
      let el = document.getElementById(elid)
      console.log(el)
      let target = getScrollTarget(el)
      let offset = el.offsetTop + 50
      let duration = 500
      setScrollPosition(target, offset, duration)
    }
  }
}
</script>

<style>

.cthrough {
  opacity: 0.8;
}

.c {
  opacity: 1;
}

</style>
