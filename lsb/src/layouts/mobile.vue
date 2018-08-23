<template>
  <q-page class="flex flex-center">
    <div  class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg.png">
      </img>
    </div>

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width">
      <div class="col-1">
      </div>
      <div class="col-10 self-center">
        <div class="text-center driveinfilled"><H4 class="q-mb-none">Long Street Backpackers is famous for its friendly and welcoming atmosphere, incredibly lush social spaces, communal activities, free meals and fantastic location. Set in a private oasis in the centre of Long Street there are literally thousands of eating, drinking and partying options right on your doorstep!</H4></div>
      </div>
    </div>
    <!-- END BLURB -->

    <div id="location">
    <!-- LOCATION LANDSCAPE -->
    <div class="row window-height window-width orientation-landscape bg-faded text-white">
      <div class="row col-6 text-center">
        <div class="col-12">
          <H2 class="row drivein justify-center q-my-sm"> LOCATION </H2>
        </div>
        <div class="col-12">
          <H4 class="driveinfilled"> 209 Long Street, Cape Town</H4>
        </div>
        <div class="col-12 driveinfilled">
          <H4> Centrally Located ...</H4>
        </div>
        <div class="col-12 driveinfilled">
          <H4> Walking distance to </H4>
        </div>
      </div>
      <div class="col-6">
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
    <!-- END LOCATION LANDSCAPE -->

    <!-- LOCATION PORTRAIT -->
    <div class="row window-height window-width orientation-portrait items-stretch bg-faded text-white">
      <div class="row text-center">
        <div class="col-12">
          <H2 class="row drivein justify-center q-mb-none"> LOCATION </H2>
        </div>
        <div class="col-12">
          <H4 class="driveinfilled q-my-none"> 209 Long Street, Cape Town</H4>
        </div>
        <div class="col-12 driveinfilled">
          <H4 class="q-my-none"> Centrally Located ...</H4>
        </div>
        <div class="col-12 driveinfilled">
          <H4 class="q-my-none"> Walking distance to </H4>
        </div>
      </div>
      <div class="window-width">
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
    <!-- END LOCATION PORTRAIT -->
    </div>

    <q-parallax src="/statics/smaller_mobile.png" :height="300">
      <H2 class="driveinfilled"> DRINK UP </H2>
    </q-parallax>

    <div id="facilities">
    <!-- FACILITIES LANDSCAPE-->
    <div class="row justify-center q-pb-xl window-height orientation-landscape">
      <div class="row col-11">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-12">
          <div class="col-5 fill2">
            <img src="/statics/bar.jpeg"></img>
          </div>
          <div class="col-1"></div>
          <div class="row col-6 q-pt-lg">
            <div class="col-4"><img width="60%" src="statics/icons/001-beer.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/011-grill.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/003-television.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/004-suitcase.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/005-wifi.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/006-credit-card.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/007-bus.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/008-stove.png"/></div>
            <div class="col-4"><img width="60%" src="statics/icons/009-holiday.png"/></div>
          </div>
          <div class="col-5 text-center q-pt-sm driveinfilled">Challenge Accepted?</div>
        </div>
      </div>
    </div>
    <!-- END FACILITIES LANDSCAPE-->

    <!-- FACILITIES PORTRAIT-->
    <div id="facilities" class="row justify-center q-pb-xl window-height orientation-portrait">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-11 justify-between q-pl-lg q-pb-lg">
          <div class="col-4"><img width="60%" src="statics/icons/001-beer.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/011-grill.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/003-television.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/004-suitcase.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/005-wifi.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/006-credit-card.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/007-bus.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/008-stove.png"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/009-holiday.png"/></div>
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
            Room 14 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 15 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 1)
          </q-card-title>
        </q-card>
        <q-card class="col-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 2)
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
            Room 14 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 15 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 1)
          </q-card-title>
        </q-card>
        <q-card class="col-6 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 2)
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS PORTRAIT -->
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
export default {
  name: 'mobile'
}
</script>
