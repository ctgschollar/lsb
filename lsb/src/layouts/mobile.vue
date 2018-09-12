<template>
  <q-page class="flex flex-center">
    <div  class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg">
      </img>
    </div>

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width">
      <div class="col-1">
      </div>
      <div class="col-10 self-center">
        <div class="text-center driveinfilled"><H4 class="q-mb-none">{{blurb}}</H4></div>
      </div>
    </div>
    <!-- END BLURB -->

    <div id="location">
    <!-- LOCATION LANDSCAPE -->
    <div id="location" class="row window-width justify-center bg-faded text-white driveinfilled orientation-landscape">
      <div class="row col-12">
        <div class="row col-12 justify-center">
          <H2 class="q-mb-none drivein"> LOCATION </H2>
        </div>
        <div class="row col-12 items-stretch">
          <div class="row col-12 text-center items-stretch">
            <div class="row col-12 justify-center">
              <div class="row col-12 justify-center">
                <H4 class="row q-mb-none">209 Long Street, Cape Town</H4>
              </div>
              <div class="col-12 justify-center  q-mb-none">
                <H4 class='q-mb-none'> {{location}} </H4>
              </div>
            </div>
            <div class="col-1"></div>
            <div class="col-10 q-mt-xl">
              <iframe
                  width="100%"
                  height="100%"
                  frameborder="0"
                  style="border:0"
                  src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
                  allowfullscreen>
              </iframe>
            </div>
            <div class="col-12 row  q-mb-none items-center">
              <H4 class="col-12 q-mb-none"> Walking distance from</H4>
              <H5 class="col-4 q-ma-none "> Table Mountain </H5>
              <H5 class="col-4 q-ma-none "> Bars & Pubs </H5>
              <H5 class="col-4 q-ma-none "> Restaurants & cafes </H5>
              <H5 class="col-4 q-ma-none "> Museums </H5>
              <H5 class="col-4 q-ma-none "> Parks </H5>
              <H5 class="col-4 q-ma-none "> Supermarkets </H5>
              <H5 class="col-4 q-ma-none "> Yoga Studios </H5>
              <H5 class="col-4 q-ma-none "> Galleries </H5>
              <H5 class="col-4 q-ma-none "> Fashion Boutiques </H5>
            </div>
          </div>

        </div>
        <div class="row col-12 justify-center text-center">
          <H5>If you’d like to arrange an airport pick-up, email us at info@longstreetbackpackers.co.za</H5>
        </div>
      </div>
    </div>
    <!-- END LOCATION LANDSCAPE -->

    <!-- LOCATION PORTRAIT -->
    <div class="row window-width orientation-portrait items-stretch bg-faded text-white">
      <div class="row text-center window-height">
        <div class="col-12">
          <H2 class="row drivein justify-center q-mb-none"> LOCATION </H2>
        </div>
        <div class="col-12">
          <H4 class="driveinfilled q-my-none"> 209 Long Street, Cape Town</H4>
        </div>
        <div class="col-12 driveinfilled ">
          <H4 class="q-my-none"> {{location}}</H4>
        </div>
        <div class="col-12 row q-my-none items-center driveinfilled">
          <H4 class="col-12 q-my-none"> Walking distance from</H4>
          <H5 class="col-6 q-ma-none q-pl-md"> Table Mountain </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Bars & Pubs </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Restaurants & cafes </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Museums </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Parks </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Supermarkets </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Yoga Studios </H5>
          <H5 class="col-6 q-ma-none q-pl-md"> Galleries </H5>
        </div>
        <div class="row col-12 justify-center text-center driveinfilled">
          <H5>If you’d like to arrange an airport pick-up, email us at info@longstreetbackpackers.co.za</H5>
        </div>
      </div>
      <div class="window-width">
        <iframe
            width="100%"
            :height="windowHeight / 2"
            frameborder="0"
            style="border:0"
            src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
            allowfullscreen>
          </iframe>
        </div>
    </div>
    <!-- END LOCATION PORTRAIT -->
    </div>

    <q-parallax src="/statics/smaller_mobile.png" :height="300">
      <H2 class="driveinfilled"> DRINK UP </H2>
    </q-parallax>

    <div id="facilities">
    <!-- FACILITIES LANDSCAPE-->
    <div class="row justify-center q-pb-xl window-height orientation-landscape driveinfilled">
      <div class="row col-11">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-12">
          <div class="col-5 fill2">
            <img src="/statics/bar.jpeg"></img>
          </div>
          <div class="col-1"></div>
          <div class="row col-6 q-pt-lg text-center">
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
    <!-- END FACILITIES LANDSCAPE-->

    <!-- FACILITIES PORTRAIT-->
    <div id="facilities" class="row justify-center q-pb-xl window-height orientation-portrait text-center driveinfilled">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-11 justify-between  q-pb-lg">
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
        <div class="col-12 q-pt-lg">
          <q-parallax src="/statics/bar-mobile.png" :height=300>
            <H4 class="driveinfilled"> CHALLENGE ACCEPTED? </H4>
          </q-parallax>
        </div>
    </div>
    <!-- END FACILITIES PORTRAIT-->
    </div>

    <q-parallax src="/statics/leafy_courtyard.png" :height=300 class="q-mt-xl orientation-landscape">
      <H2 class="driveinfilled"> RECOVER </H2>
    </q-parallax>

    <div id="rooms">
    <!-- ROOMS LANDSCAPE-->
    <div class="row window-height justify-center q-pt-lg  orientation-landscape">
      <div class="row col-12">
        <div class="row col-12 justify-center">
          <div class="drivein">
            <H2 class="drivein"> ROOMS </H2>
          </div>
        </div>
        <!--<div class="col-6">
        </div>-->

        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/single/single1.jpeg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Single Room
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/twin/twin1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Twin Room
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_14/dorm_14_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Double Room
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            4 Bed Dorm
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            6 Bed Room
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            10 Bed Room
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS LANDSCAPE -->

    <!-- ROOMS PORTRAIT-->
    <div id="rooms" class="row window-heightjustify-center q-pt-lg  orientation-portrait">
      <div class="row col-12">
        <div class="row col-12 justify-center">
          <div class="drivein">
            <H2 class="drivein"> ROOMS </H2>
          </div>
        </div>
        <!--<div class="col-6">
        </div>-->

        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/single/single1.jpeg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Single Room
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/twin/twin1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Twin Room
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_14/dorm_14_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Double Room
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            4 Bed Dorm
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            6 Bed Room
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            10 Bed Room
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS PORTRAIT -->
    </div>

    <div class="row window-width items-center  bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled q-pt-xl">{{review1}}</H4>
      </div>
    </div>

    <q-parallax src="statics/bar.jpeg.png" :height=600 class="q-pt-xl">

    </q-parallax>

    <div class="row window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review2}}</H4>
      </div>
    </div>

    <q-parallax src="statics/braai courtyard.jpeg.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review3}}</H4>
      </div>
    </div>

    <q-parallax src="statics/Beer Pong 2.jpg.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review4}}</H4>
      </div>
    </div>

    <q-parallax src="statics/ismaller.png" :height=600>
    </q-parallax>

    <div class="row window-width items-center bg-faded text-white">
      <div class="col-2">
      </div>
      <div class="col-8">
        <H4 class="text-center driveinfilled">{{review5}}</H4>
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
    overflow: hidden
}
.fill img {
    flex-shrink: 0;
    max-width: 260%;
    max-height: 150%
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
  name: 'mobile',
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
