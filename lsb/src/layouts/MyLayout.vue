<template>
  <div>
    <q-layout v-if='desktop' view="hhh lpr FFF">
      <q-layout-header reveal :reveal-offset="windowHeight + 150" class="bg-white" >
        <div class="drivein row q-pr-lg" ref="header">
          <div class="col-2 q-pa-sm">
            <img src='statics/logo.png'>
          </div>
          <div class="row col-10">
          <div v-if="windowHeight - windowScroll < headerHeight * 2" class="col-md-12 col-lg-6 q-pb-md row items-end justify-end">
            <form id="check_availability" action="https://hotels.cloudbeds.com/booking/reservation/A9p5sR" method="post">
              <div class="container row justify-around">
                <q-datetime color="black"  flat class="q-pr-sm datepicker_input hasDatepicker" type="date" v-model="date" name="widget_date" id="date_1" @change="updateDate"/>
                <q-datetime color="black" flat type="date" class="datepicker_input hasDatepicker" name="widget_date_to" v-model="dateTo" id="date_2" @change="updateDateTo"/>
                <input name="widget_date" type="hidden" maxlength="10" :value="dateStr" class="datepicker_input hasDatepicker" id="date_1">
                <input name="widget_date_to" type="hidden" maxlength="10" :value="dateToStr" class="datepicker_input hasDatepicker" id="date_2">
                <input type="hidden" value="d/m/Y" name="date_format">
                <q-btn type="submit" hidden name="bf_submit" label="BOOK NOW" class="bg-black" text-color="white" flat dense size="xl" id="book"/>
                <q-btn label="Book Now" class="bg-black" text-color="white" flat dense size="xl" @click='customDialogModel=true'/>
                <q-dialog
                  v-model="customDialogModel"
                  class="driveinfilled"
                >
                  <span slot="title">Before you book</span>
                  <span slot="message" class="text-black">
                    <p>All guests <b>must</b> produce a valid passport on check in.</p>
                    <p>This includes South African Guests.</p>
                    <p><b>No other form of ID will be accepted</b></p></span>

                  <template slot="buttons" slot-scope="props">
                    <q-btn color="black"><label for="book">Continue Booking</label></q-btn>
                    <q-btn color="white" class="text-black" label="Cancel" @click="props.cancel" />
                  </template>
                </q-dialog>
              </div>
            </form>
          </div>
          <div v-if="windowHeight - windowScroll < headerHeight * 2" class="col-md-12 col-lg-6 row items-end justify-end">
            <q-btn color="dark" flat label="Facilities"
             @click="scrollToElement('facilities')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Location"
            @click="scrollToElement('location')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Rooms"
            @click="scrollToElement('rooms')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Contact Us"
            @click="scrollToElement('contactus')"
            size="xl" class="q-pb-md"/>
          </div>
          <div v-else class="col-12 row items-end justify-end">
            <q-btn color="dark" flat label="Facilities"
             @click="scrollToElement('facilities')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Location"
            @click="scrollToElement('location')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Rooms"
            @click="scrollToElement('rooms')"
            size="xl" class="q-pb-md"/>
            <q-btn color="dark" flat label="Contact Us"
            @click="scrollToElement('contactus')"
            size="xl" class="q-pb-md"/>
          </div>
          </div>
        </div>
      </q-layout-header>

      <q-page-container>
        <router-view :d='date' :d2='dateTo' @d='setDate' @d2='setDateTo'/>
      </q-page-container>

      <q-btn
        v-if='windowScroll > 500'
        round
        color="dark"
        v-back-to-top.animate="{offset: 500, duration: 500}"
        class="fixed"
        style="right: 18px; bottom: 18px"
      >
        <q-icon name="arrow_upward" />
      </q-btn>

    </q-layout>
    <q-layout v-else view="hhh lpr fFf">
      <q-layout-header reveal :reveal-offset="150" class="bg-white" >
        <div class="drivein row" ref="header">
          <div class="col-9 q-pl-sm q-py-sm">
            <img src='statics/logo.png'>
          </div>
          <div class="row items-start col-3 justify-end">
            <q-btn flat icon="menu" class="driveinfilled">
              <q-popover>
                <q-list separator link class="q-py-none">
                  <q-item v-close-overlay>
                    <q-btn color="dark" flat label="Facilities"
                        @click="scrollToElement('facilities')"
                        size="lg" class="drivein"/>
                  </q-item>
                  <q-item v-close-overlay>
                        <q-btn color="dark" flat label="Location"
                        @click="scrollToElement('location')"
                        size="lg" class="drivein"/>
                  </q-item>
                   <q-item v-close-overlay>
                        <q-btn color="dark" flat label="Rooms"
                        @click="scrollToElement('rooms')"
                        size="lg" class="drivein"/>
                  </q-item>
                  <q-item v-close-overlay>
                    <q-btn color="dark" flat no-wrap label="Contact Us"
                    @click="scrollToElement('contactus')"
                    size="lg" class="drivein"/>
                  </q-item>
                </q-list>
              </q-popover>
            </q-btn>
          </div>
        </div>
      </q-layout-header>

      <q-page-container>
        <router-view :d='date' :d2='dateTo' @d='setDate' @d2='setDateTo'/>
      </q-page-container>

      <q-layout-footer class="bg-white drivein" style="opacity:0.7" reveal :reveal-offset="150">
        <div v-if="windowScroll < windowHeight/3" class="row justify-end q-py-sm bg-red">
        <div class="col-8"></div>
        <div class="col-4 row justify-center q-pr-lg">
          <b>BOOK NOW</b>
          <q-icon name="arrow_downward"/>
        </div>
        </div>
        <form id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
          <div class="container row justify-around">
            <q-datetime color="black"  flat class="q-pr-sm datepicker_input hasDatepicker" type="date" v-model="date" name="widget_date" id="date_1" @change="updateDate"/>
            <q-datetime color="black" flat type="date" class="datepicker_input hasDatepicker" name="widget_date_to" v-model="dateTo" id="date_2" @change="updateDateTo"/>
            <input name="widget_date" type="hidden" maxlength="10" :value="dateStr" class="datepicker_input hasDatepicker" id="date_1">
            <input name="widget_date_to" type="hidden" maxlength="10" :value="dateToStr" class="datepicker_input hasDatepicker" id="date_2">
            <input type="hidden" value="d/m/Y" name="date_format">
            <q-btn type="submit" hidden name="bf_submit" label="BOOK NOW" class="bg-black" text-color="white" flat dense size="xl" id="book"/>
            <q-btn icon="event" class="bg-black" text-color="white" flat dense size="xl" @click='customDialogModel=true'/>
            <q-dialog
              v-model="customDialogModel"
              class="driveinfilled"
            >
              <span slot="title">Before you book</span>
              <span slot="message" class="text-black">
                <p>All guests <b>must</b> produce a valid passport on check in.</p>
                <p>This includes South African Guests.</p>
                <p><b>No other form of ID will be accepted</b></p></span>

              <template slot="buttons" slot-scope="props">
                <q-btn color="black" class="driveinfilled"><label for="book">Continue Booking</label></q-btn>
                <q-btn color="white" class="text-black driveinfilled" label="Cancel" @click="props.cancel" />
              </template>
            </q-dialog>
          </div>
        </form>
      </q-layout-footer>

      <q-btn
        v-if='windowScroll > 500'
        round
        color="black"
        v-back-to-top.animate="{offset: 500, duration: 500}"
        class="fixed"
        style="right: 18px; bottom: 60px; opacity:0.7"
      >
        <q-icon name="arrow_upward" />
      </q-btn>

    </q-layout>
  </div>
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
      headerHeight: 0,
      customDialogModel: false,
      nav: true
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
    setDate (date){
      this.$set(this, 'date', date)
      this.updateDate()
    },
    setDateTo (dateTo){
      this.$set(this, 'dateTo', dateTo)
      this.updateDateTo()
    },
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
