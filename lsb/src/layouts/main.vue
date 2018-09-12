<template>
  <q-page class="flex flex-center">
    <q-parallax src="statics/banner_pic.jpeg.png" :height=windowHeight >
    </q-parallax>
    <!--<div class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg.png">
      </img>
    </div>-->

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled">{{blurb}}</H3>
      </div>
    </div>
    <!-- END BLURB -->

    <!-- LOCATION -->
    <div id="location" class="row window-height window-width justify-center bg-faded text-white driveinfilled">
      <div class="row col-xl-10 col-lg-11">
        <div class="row col-12 justify-center">
          <H2 class="q-mb-none drivein"> LOCATION </H2>
        </div>
        <div class="row col-12 items-stretch" style="height:70%">
          <div class="row col-6 text-center items-stretch">
            <div class="row col-12 justify-center">
              <div class="row col-12 justify-center">
                <H4 class="row q-mb-none">209 Long Street, Cape Town</H4>
              </div>
              <div class="col-12 justify-center q-mx-lg  q-mb-none">
                <H4> {{location}} </H4>
              </div>
            </div>
            <div class="col-12 row q-ml-lg  q-my-none items-center">
              <H4 class="col-12 q-my-none text-left"> Walking distance from :</H4>
              <H5 class="col-4 q-ma-none q-pl-md"> Table Mountain </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Bars & Pubs </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Restaurants & cafes </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Museums </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Parks </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Supermarkets </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Yoga Studios </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Galleries </H5>
              <H5 class="col-4 q-ma-none q-pl-md"> Fashion Boutiques </H5>
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

    <q-parallax src="/statics/ismaller.png" :height=700>
      <H4 class="driveinfilled"> DRINK UP </H4>
    </q-parallax>

    <!-- FACILITIES -->
    <div id="facilities" class="row q-pb-xl items-start window-width driveinfilled">
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
          <H5 class="col-xl-5 col-md-4 text-center q-pt-sm driveinfilled">Challenge Accepted?</H5>
        </div>
      </div>
    </div>
    <!-- END FACILITIES -->

    <q-parallax src="/statics/balcony evening.jpeg.png" :height=700 class="q-mt-xl">
      <H4 class="driveinfilled"> Maybe One More </H4>
    </q-parallax>

    <!-- ROOMS -->
    <div id="rooms" class="row window-width justify-center items-start q-mb-xl">
      <div class="row col-10">
        <div class="row col-12 justify-center">
          <div class="drivein">
            <H2 class="drivein"> ROOMS </H2>
          </div>
        </div>
        <!--<div class="col-6">
        </div>-->

        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/single/single1.jpeg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Single Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/twin/twin1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Twin Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_14/dorm_14_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Double Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            4 Bed Dorm
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            6 Bed Room
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            10 Bed Room
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS -->

    <div class="row window-width items-center  bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled q-pt-xl">{{review1}}</H3>
      </div>
    </div>

    <q-parallax src="statics/bar.jpeg.png" :height=600 class="q-pt-xl">

    </q-parallax>

    <div class="row window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled">{{review2}}</H3>
      </div>
    </div>

    <q-parallax src="statics/braai courtyard.jpeg.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled">{{review3}}</H3>
      </div>
    </div>

    <q-parallax src="statics/Beer Pong 2.jpg.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled">{{review4}}</H3>
      </div>
    </div>

    <q-parallax src="statics/ismaller.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H3 class="text-center driveinfilled">{{review5}}</H3>
      </div>
    </div>


  </q-page>
</template>

<style>

.drivein {
  font-family: 'driveInShadow';
}

.driveinfilled {
  font-family: 'driveInFilled'
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
import blurb from '../statics/text/blurb.txt'
import location from '../statics/text/Location.txt'
import review1 from '../statics/text/review1.txt'
import review2 from '../statics/text/review2.txt'
import review3 from '../statics/text/review3.txt'
import review4 from '../statics/text/review4.txt'
import review5 from '../statics/text/review5.txt'

export default {
  name: 'page',
  data: function () {
    return {
      blurb: blurb,
      location: location,
      review1: review1,
      review2: review2,
      review3: review3,
      review4: review4,
      review5: review5,
      windowHeight: window.innerHeight
    }
  }
}
</script>
