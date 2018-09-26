<template>
  <q-page class="flex flex-center absolute-top">
    <q-parallax src="statics/banner_pic.jpeg.png" :height='windowHeight - 50'>

    </q-parallax>
    <div class="row window-width bg-white drivein bg-red items-center" style="height:50px">
      <div class="col-1"></div>
      <div class="col-9">
        <form id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
          <div class="container row justify-around">
          <q-datetime color="black" flat class="q-pr-sm datepicker_input hasDatepicker " type="date" v-model="date" name="widget_date" id="date_1" @change="updateDate"/>
          <q-datetime color="black" flat type="date" class="datepicker_input hasDatepicker" name="widget_date_to" v-model="dateTo" id="date_2" @change="updateDateTo"/>
          <input name="widget_date" type="hidden" maxlength="10" :value="dateStr" class="datepicker_input hasDatepicker" id="date_1">
          <input name="widget_date_to" type="hidden" maxlength="10" :value="dateToStr" class="datepicker_input hasDatepicker" id="date_2">
          <input type="hidden" value="d/m/Y" name="date_format">
          <q-btn id="book" type="submit"  hidden name="bf_submit" label="BOOK NOW"/>
          <q-btn label="Book Now" dense size="lg" @click='customDialogModel=true'/>
          </div>

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
        </form>
      </div>
    </div>

    <!--<div class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg.png">
      </img>
    </div>-->

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{blurb}}</H4>
      </div>
    </div>
    <!-- END BLURB -->

    <!-- LOCATION -->
    <div id="location" class="row window-height window-width justify-center bg-faded text-white drivein">
      <div class="row col-xl-10 col-lg-11">
        <div class="row col-12 justify-center">
          <H2 class="q-mb-none drivein"> LOCATION </H2>
        </div>
        <div class="row col-12 items-stretch" style="height:70%">
          <div class="row col-6 text-center items-stretch">
            <div class="row col-12 justify-center">
              <div class="row col-12">
                <H5 class="row q-mb-none text-left">209 Long Street, Cape Town</H5>
              </div>
              <div class="col-12 justify-center q-mx-lg  q-mb-none text-left">
                <H5> {{location}} </H5>
              </div>
            </div>
            <div class="col-12 row q-ml-lg  q-my-none items-center text-left">
              <H5 class="col-12 q-my-none text-left"> Walking distance from :</H5>
              <H6 class="col-4 q-ma-none q-pl-md"> Table Mountain </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Bars & Pubs </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Restaurants & cafes </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Museums </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Parks </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Supermarkets </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Yoga Studios </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Galleries </H6>
              <H6 class="col-4 q-ma-none q-pl-md"> Fashion Boutiques </H6>
            </div>
          </div>
          <div class="col-1"></div>
          <div class="col-5 q-mt-xl">
            <iframe
                width="100%"
                height="100%"
                frameborder="0"
                style="border:0"
                src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
                allowfullscreen>
            </iframe>
          </div>
        </div>
        <div class="row col-12 justify-center text-center">
          <H5>If you’d like to arrange an airport pick-up, email us at info@longstreetbackpackers.co.za</H5>
        </div>
      </div>
    </div>
    <!-- END LOCATION -->

    <q-parallax src="/statics/ismaller.png" :height=windowHeight>
    </q-parallax>

    <!-- FACILITIES -->
    <div id="facilities" class="row q-pb-xl items-start window-width drivein">
      <div class="row col-12">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-12 q-pt-lg">
          <div class="col-xl-5 col-md-4 fill2">
            <img src="/statics/bar.jpeg"></img>
          </div>

          <div class="row col-xl-7 col-md-8 q-pl-xl q-pt-lg text-center">
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/001-beer.png"/>
              <div class="col-12">Lively traveller’s bar</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/011-grill.png"/>
              <div class="col-12">Braai/BBQ</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/003-television.png"/>
              <div class="col-12">TV room with DSTV</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/004-suitcase.png"/>
              <div class="col-12">Luggage Storage</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/005-wifi.png"/>
              <div class="col-12">Fibre-speed Wifi</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/006-credit-card.png"/>
              <div class="col-12">2 x Balconies for the flaneur</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/007-bus.png"/>
              <div class="col-12">Lush courtyard oasis</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/008-stove.png"/>
              <div class="col-12">Large communal Kitchen</div>
            </div>
            <div class="col-4 row justify-center items-center">
              <img width="30%" src="statics/icons/009-holiday.png"/>
              <div class="col-12">The friendliest hostel in Cape Town!</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- END FACILITIES -->

    <q-parallax src="/statics/balcony evening.jpeg.png" :height=windowHeight class="q-mt-xl">
    </q-parallax>

    <!-- ROOMS -->
    <div id="rooms" class="row window-width justify-center items-start q-mb-xl drivein">
      <div class="row col-10">
        <div class="row col-12 justify-center">
          <div class="drivein">
            <H2 class="drivein q-mb-md"> ROOMS </H2>
          </div>
        </div>
        <div class="col-12 q-pb-sm">
        All guests must produce a valid <b>passport</b> on check in. Including South Africans.
        </div>

        <q-card class="col-sm-4 q-pa-sm ">
          <q-card-media class="fill3">
            <img src="/statics/rooms/single/single1.jpeg">
          </q-card-media>
          <q-card-title>
            Single Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/twin/twin1.jpg">
          </q-card-media>
          <q-card-title>
            Twin Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_14/dorm_14_1.jpg">
          </q-card-media>
          <q-card-title>
            Double Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title>
            4 Bed Dorm
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title>
            6 Bed Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title>
            10 Bed Room
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS -->

    <!-- REVIEWS -->
    <div class="row window-width items-center window-height bg-black text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled q-pt-xl">{{review1}}</H4>
      </div>
    </div>

    <q-parallax src="statics/bar.jpeg.png" :height=windowHeight class="q-pt-xl">

    </q-parallax>

    <div class="row window-width window-height items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review2}}</H4>
      </div>
    </div>

    <q-parallax src="statics/braai courtyard.jpeg.png" :height=windowHeight>
    </q-parallax>

    <div class="row window-width items-center bg-black text-white window-height">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review3}}</H4>
      </div>
    </div>

    <q-parallax src="statics/Beer Pong 2.jpg.png" :height=windowHeight>
    </q-parallax>

    <div class="row window-width items-center window-height">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review4}}</H4>
      </div>
    </div>

    <q-parallax src="statics/ismaller.png" :height=windowHeight>
    </q-parallax>

    <div class="row window-width items-center bg-black text-white window-height">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review5}}</H4>
      </div>
    </div>
    <!-- END REVIEWS -->

    <!-- CONTACT US -->
    <div class="row window-width items-center  driveinfilled">
      <div class="col-1"></div>
      <div class="col-8 q-pl-xl q-pb-xl">
        <H6>Contact Us</H6>
        <p> Phone : +27 (0) 21 423 0615 </p>
        <p> Email : info@longstreetbackpackers.co.za </p>
        <p> 209 Long street, Cape Town </p>
      </div>
      <div style="height : 100"></div>
    </div>

    <!-- END CONTACT US -->

  </q-page>
</template>

<style>

.drivein {
  font-family: 'BEBAS';
}

.driveinfilled {
  font-family: 'roman'
}

.fill {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    background-position: center;
}
.fill img {
    flex-shrink: 0;
    max-width: 155%;
    max-height: 130%
}

.fill2 {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    background-position: center;
}
.fill2 img {
    flex-shrink: 0;
    max-width: 130%;
    max-height: 100%
}

.fill3 {
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    background-position: center;
}
.fill3 img {
    flex-shrink: 0;
    max-width: 140%;
    max-height: 100%
}

</style>

<script>
import {date} from 'quasar'
import blurb from '../statics/text/blurb.txt'
import location from '../statics/text/Location.txt'
import review1 from '../statics/text/review1.txt'
import review2 from '../statics/text/review2.txt'
import review3 from '../statics/text/review3.txt'
import review4 from '../statics/text/review4.txt'
import review5 from '../statics/text/review5.txt'

export default {
  name: 'page',
  props: ['d', 'd2'],
  data: function () {
    return {
      blurb: blurb,
      location: location,
      review1: review1,
      review2: review2,
      review3: review3,
      review4: review4,
      review5: review5,
      windowHeight: window.innerHeight,
      date: date.addToDate(new Date(), { days: 1 }),
      dateTo: date.addToDate(new Date(), { days: 4 }),
      dateStr: date.formatDate(date.addToDate(new Date(), { days: 1 }), 'DD/MM/YYYY'),
      dateToStr: date.formatDate(date.addToDate(new Date(), { days: 4 }), 'DD/MM/YYYY'),
      customDialogModel: false
    }
  },
  created() {
    this.$set(this, 'date', this.d)
    this.$set(this, 'dateTo', this.d2)
    this.updateDate()
    this.updateDateTo()
  },
  mounted() {
    this.$watch('d', d => {
      this.$set(this, 'date', this.d)
      this.$set(this, 'dateStr', date.formatDate(this.date, 'DD/MM/YYYY'))
    })

    this.$watch('d2', d2 => {
      this.$set(this, 'dateTo', this.d2)
      this.$set(this, 'dateToStr', date.formatDate(this.dateTo, 'DD/MM/YYYY'))
    })
  },
  methods: {
    updateDate (){
      this.$set(this, 'dateStr', date.formatDate(this.date, 'DD/MM/YYYY'))
      this.$emit('d', this.date)
    },
    updateDateTo (){
      this.$set(this, 'dateToStr', date.formatDate(this.dateTo, 'DD/MM/YYYY'))
      this.$emit('d2', this.dateTo)
    }
  }
}
</script>
