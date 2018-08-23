<template>
  <q-page class="flex flex-center">
    <div class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg.png">
      </img>
    </div>

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width items-center">
      <div class="col-3">
      </div>
      <div class="col-6">
        <H4 class="text-center driveinfilled">Long Street Backpackers is famous for its friendly and welcoming atmosphere, incredibly lush social spaces, communal activities, free meals and fantastic location. Set in a private oasis in the centre of Long Street there are literally thousands of eating, drinking and partying options right on your doorstep!</H4>
      </div>
    </div>
    <!-- END BLURB -->

    <!-- LOCATION -->
    <div id="location" class="row window-height window-width justify-center bg-faded text-white">
      <div class="row col-xl-10 col-lg-11">
        <div class="row col-5 text-center">
          <div class="row col-12 justify-center">
            <H2 class="q-mb-none drivein"> LOCATION </H2>
          </div>
          <div class="row col-12 justify-center">
            <H4 class="row driveinfilled">209 Long Street, Cape Town</H4>
          </div>
          <div class="row col-12 justify-center">
            <H4 class="driveinfilled"> Centrally Located </H4>
          </div>
          <div class="col-12 q-mt-xl">
            <H4 class="driveinfilled">Walking distance to :</H4>
          </div>
        </div>
        <div class="col-1"></div>
        <div class="col-6 q-mt-xl q-pt-xl">
          <div class=" q-pt-xl">
          </div>
          <iframe
              width="100%"
              height="80%"
              frameborder="0"
              style="border:0"
              src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
              allowfullscreen>
          </iframe>
        </div>
      </div>
    </div>
    <!-- END LOCATION -->

    <q-parallax src="/statics/ismaller.png" :height=700>
      <H4 class="driveinfilled"> DRINK UP </H4>
    </q-parallax>

    <!-- FACILITIES -->
    <div id="facilities" class="row justify-center q-pb-xl items-start">
      <div class="row col-10">
        <div class="row col-12 justify-center">
          <H2  class="drivein"> FACILITIES </H2>
        </div>
        <div class="row col-12 q-pt-lg">
          <div class="col-5 fill2">
            <img src="/statics/bar-mobile.png"></img>
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
          <H4 class="col-5 text-center q-pt-sm driveinfilled">Challenge Accepted?</H4>
        </div>
      </div>
    </div>
    <!-- END FACILITIES -->

    <q-parallax src="/statics/leafy_courtyard.png" :height=700 class="q-mt-xl">
      <H4 class="driveinfilled"> RECOVER </H4>
    </q-parallax>

    <!-- ROOMS -->
    <div id="rooms" class="row window-height window-width justify-center items-start">
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
            Room 14 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/dorm_15/dorm_15_1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 15 (Dorm)
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16first/16first1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 1)
          </q-card-title>
        </q-card>
        <q-card class="col-sm-4 q-pa-sm">
          <q-card-media class="fill3">
            <img src="/statics/rooms/16second/16second1.jpg">
          </q-card-media>
          <q-card-title class="driveinfilled">
            Room 16 (Dorm 2)
          </q-card-title>
        </q-card>
      </div>
    </div>
    <!-- END ROOMS -->


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
export default {
  name: 'page'
}
</script>
