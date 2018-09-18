<template>
  <q-layout view="hhh lpr FFF">
    <q-layout-header reveal :reveal-offset="windowHeight + 100" class="bg-white" >
      <div class="driveinfilled q-mx-lg" ref="header">
        <div>
          <H2 v-if="desktop" class="q-my-md">LONG STREET BACKPACKERS</H2>
          <H4 v-else class="q-my-none">LONG STREET BACKPACKERS</H4>
        </div>
        <div :class="desktop ? 'col-10' : 'col-12'">
          <div v-if="windowHeight - windowScroll < headerHeight * 2" class="float-left">
            <form v-if="desktop" id="check_availability" action="https://hotels.cloudbeds.com/booking/reservation/A9p5sR" method="post">
              <div class="container row justify-around">
                <q-datetime color="dark"  flat class="q-pr-sm datepicker_input hasDatepicker" type="date" v-model="date" name="widget_date" id="date_1" @change="updateDate"/>
                <q-datetime color="dark" flat type="date" class="datepicker_input hasDatepicker" name="widget_date_to" v-model="dateTo" id="date_2" @change="updateDateTo"/>
                <input name="widget_date" type="hidden" maxlength="10" :value="dateStr" class="datepicker_input hasDatepicker" id="date_1">
                <input name="widget_date_to" type="hidden" maxlength="10" :value="dateToStr" class="datepicker_input hasDatepicker" id="date_2">
                <input type="hidden" value="d/m/Y" name="date_format">
                <q-btn type="submit" name="bf_submit" label="BOOK NOW" color="dark" flat dense size="xl"/>
              </div>
            </form>
            <form v-else id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
              <div class="container row justify-around">
                <q-datetime color="dark"  flat class="q-pr-sm datepicker_input hasDatepicker" type="date" v-model="date" name="widget_date" id="date_1" @change="updateDate"/>
                <q-datetime color="dark" flat type="date" class="datepicker_input hasDatepicker" name="widget_date_to" v-model="dateTo" id="date_2" @change="updateDateTo"/>
                <input name="widget_date" type="hidden" maxlength="10" :value="dateStr" class="datepicker_input hasDatepicker" id="date_1">
                <input name="widget_date_to" type="hidden" maxlength="10" :value="dateToStr" class="datepicker_input hasDatepicker" id="date_2">
                <input type="hidden" value="d/m/Y" name="date_format">
                <q-btn type="submit" name="bf_submit" label="BOOK NOW" color="dark" flat dense/>
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
      date: date.addToDate(new Date(), { days: 1 }),
      dateTo: date.addToDate(new Date(), { days: 4 }),
      dateStr: date.formatDate(date.addToDate(new Date(), { days: 1 }), 'DD/MM/YYYY'),
      dateToStr: date.formatDate(date.addToDate(new Date(), { days: 4 }), 'DD/MM/YYYY'),
      facilities: false,
      location: false,
      rooms: false,
      windowHeight: window.innerHeight,
      windowScroll: window.scrollY,
      headerHeight: 0

    }
  },
  created() {
    if (this.desktop) {
        this.$router.push('/main');
    }
    else {
        this.$router.push('/mobile');
    }
    window.addEventListener('scroll', this.handleScroll)
  },
  mounted(){
    this.$set(this, 'headerHeight', this.$refs['header'].clientHeight)
  },
  methods: {
    updateDate (){
      this.$set(this, 'dateStr', date.formatDate(this.date, 'DD/MM/YYYY'))
    },
    updateDateTo (){
      this.$set(this, 'dateToStr', date.formatDate(this.dateTo, 'DD/MM/YYYY'))
    },
    embiggen (event) {
      console.log('yo')
      console.log(event)
    },
    handleScroll (event) {
      this.$set(this, 'windowScroll', window.scrollY)
    },
    scrollToElement (elid) {
      let el = document.getElementById(elid)
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
