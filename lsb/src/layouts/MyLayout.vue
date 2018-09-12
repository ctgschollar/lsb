<template>
  <q-layout view="hhh lpr FFF">
    <q-layout-header reveal :reveal-offset="50" class="bg-white">
      <div class="driveinfilled q-mx-lg">
        <div>
          <H2 v-if="desktop" class="q-my-md">LONG STREET BACKPACKERS</H2>
          <H4 v-else class="q-my-none">LONG STREET BACKPACKERS</H4>
        </div>
        <div :class="desktop ? 'col-10' : 'col-12'">
          <div class="float-left">
            <form v-if="desktop" id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
              <div class="container row justify-around">
                <q-datetime color="dark"  flat class="hidden q-pr-sm" type="date" v-model="date" name="widget_date" id="date_1"/>

                <q-datetime color="dark"  flat class="hidden" type="date" name="widget_date_to" v-model="dateTo" id="date_2"/>
                <input type="hidden" value="d/m/Y" name="date_format">
                <q-btn color="dark" size="xl" dense flat type="submit" name="bf_submit" label="BOOK NOW"/>
                <!--<div class="q-title text-white vertical-middle"> BOOK NOW </div>-->
                <div class="clear_floats"></div>
              </div>
            </form>
            <form v-else id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
              <div class="container row justify-around">
                <q-datetime  color="dark" dense flat class="hidden" type="date" v-model="date" name="widget_date" id="date_1"/>
                <q-datetime class="hidden" color="dark" dense flat type="date" name="widget_date_to" v-model="dateTo" id="date_2"/>
                <input type="hidden" value="d/m/Y" name="date_format">
                <q-btn color="dark" dense flat type="submit" name="bf_submit" size="lg" label="BOOK NOW"/>
                <div class="clear_floats"></div>
              </div>
            </form>
          </div>
          <div v-if="desktop" class="float-right">
            <q-btn color="dark" flat label="Facilities"
             @click="scrollToElement('facilities')"
            size="xl"
            @mouseenter.native="facilities = true"
            @mouseleave.native="facilities = false"/>
            <q-btn color="dark" flat label="Location"
            @click="scrollToElement('location')"
            size="xl"
            @mouseenter.native="location = true"
            @mouseleave.native="location = false"/>
            <q-btn color="dark" flat label="Rooms"
            @click="scrollToElement('rooms')"
            size="xl"
            @mouseenter.native="rooms = true"
            @mouseleave.native="rooms = false"/>
          </div>
        </div>
      </div>
    </q-layout-header>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { date, scroll } from 'quasar'

const { getScrollTarget, setScrollPosition } = scroll

export default {
  name: 'MyLayout',
  data () {
    return {
      desktop: this.$q.platform.is.desktop,
      state: true,
      footer: true,
      header: true,
      date: new Date(),
      dateTo: date.addToDate(new Date(), { days: 1 }),
      facilities: false,
      location: false,
      rooms: false
    }
  },
  created() {
    if (this.desktop) {
        this.$router.push('/main');
    }
    else {
        this.$router.push('/mobile');
    }
  },
  methods: {
    embiggen (event) {
      console.log('yo')
      console.log(event)
    },
    scrollToElement (elid) {
      let el = document.getElementById(elid)
      console.log(el)
      let target = getScrollTarget(el)
      let offset = el.offsetTop
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
