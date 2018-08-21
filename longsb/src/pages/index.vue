<template>
  <q-page class="flex justify-center">
    <div class="relative-position full">
      <q-carousel :autoplay="5000" :infinite="true" class="window-height">
        <q-carousel-slide img-src="statics/room.jpg" w="500" />
        <q-carousel-slide img-src="statics/P4130376.jpg"/>
        <q-carousel-slide img-src="statics/P4130391.jpg"/>
      </q-carousel>
      <a href="tel:+27214230615">
        <q-btn fab color="primary" icon="call" class="absolute" style="top: 10%; right: 5%; transform: translateY(-50%);" />
      </a>
      <a href="https://www.facebook.com/Long-Street-Backpackers-Adventure-with-friends-in-the-heart-of-Cape-Town-134709429919748/">
        <img src="statics/flogo_RGB_HEX-144.png" width="53px" class="absolute" style="top: 23%; right: 5%; transform: translateY(-50%);"/>
      </a>
      <a href="https://www.instagram.com/longstreetbackpackers/?hl=en">
        <img src="statics/glyph-logo_May2016.png" width="53px" class="absolute" style="top: 36%; right: 5%; transform: translateY(-50%);"/>
      </a>
      <a href="https://www.tripadvisor.co.za/Hotel_Review-g312659-d562306-Reviews-Long_Street_Backpackers-Cape_Town_Central_Western_Cape.html">
        <img src="statics/tripadvisor-logo.png" width="53px" class="absolute" style="top: 49%; right: 5%; transform: translateY(-50%);"/>
      </a>
    </div>
    <div class="container row justify-around full">
      <div class="col-sm-5">
        <div class="row justify-center">
          <div id="about" class="col-12"><img src="statics/code_of_arms_big.jpg" class="col-1"/></div>
          <div class="col-12 q-px-lg" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean placerat ipsum in sapien bibendum, at lobortis ante tincidunt. Proin et quam sed ante tristique viverra. Suspendisse facilisis mauris luctus tellus pulvinar vehicula. Duis a viverra orci. Suspendisse lacinia ac tellus sit amet varius. Integer eu lobortis lectus, tempus facilisis massa. Quisque dictum vestibulum fermentum. Duis porta ligula sagittis egestas laoreet. Etiam pulvinar felis ut elit tristique scelerisque. Cras quis enim nisi. Quisque pellentesque molestie fermentum. Suspendisse ac nisi laoreet, fringilla mauris nec, congue nisi. Vivamus at neque ut justo molestie semper. Quisque nec urna sed tellus varius elementum. Fusce elementum mauris sit amet efficitur pellentesque. Aliquam sed commodo tortor.</div>
          <div id="facilities" class="col-12 row justify-center"><H3>Facilities</H3></div>
          <div class="col-12 row q-px-md q-pl-lg">
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/001-toast.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> Crazy Bar </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/002-stove.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> Kitchen </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/003-lockers.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> Storage </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/004-shower.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> 16 Showers </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/005-desk-bell.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> 12 am Checkout </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/006-router.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> WiFi </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/007-barbecue.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> BBQ </div></div>
            <div class="col-2 q-py-md"><img width="80%" src="statics/icons/008-pint.svg"/></div>
            <div class="col-4"><div class="col-4 q-headline vcent"> PARTY </div></div>
          </div>
        </div>
      </div>
      <div class="col-sm-7">
      <!--<vue-instagram token="5450403056.d0833b5.9f78d8db81c5431488405ca186663590" username="christopherschollar" :count="5" :tags="['hashtag1', 'hashtag2']">
        <template slot="feeds" slot-scope="props">
          <li class="fancy-list"> {{ props.feed.link }} </li>
        </template>
        <template slot="error" slot-scope="props">
          <div class="fancy-alert"> {{ props.error.error_message }} </div>
        </template>
      </vue-instagram>-->
      </div>
      <div id="location" class="row col-12">
        <div class="col-12"><div class="row justify-center"><H3> Location </H3></div></div>
        <div class="col-sm-4 q-pl-md">
          <iframe
            width="100%"
            height="100%"
            frameborder="0"
            style="border:0"
            src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
            allowfullscreen>
          </iframe>
        </div>
        <div class="row col-sm-4">
          <div class="col-12 q-pa-md">LOCATED ON LONG STREET IN THE HEART OF PARTY TOWN</div>
          <div class="col-12 q-pa-md">TO GET HERE FROM THE AIRPORT</div>
        </div>
        <div class="col-sm-4">
          <img width="100%" src="statics/longstreet_house_home.png"/>
        </div>
      </div>
      <div id="rooms" class="row col-12">
        <div class="col-12"><div class="row justify-center"><H3> Rooms </H3></div></div>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/room.jpg">
          </q-card-media>
          <q-card-title>
            Single Room
          </q-card-title>
          <q-card-main>
          <p>R 350</p>
          <p class="text-faded">
            For the sophisticated traveler that prefers privacy while getting laid.
          </p>
          </q-card-main>
         </q-card>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/room.jpg">
          </q-card-media>
          <q-card-title>
            Double Room
          </q-card-title>
          <q-card-main>
          <p>R 420</p>
          <p class="text-faded">
            For the sophisticated traveler that prefers privacy while getting
            laid on a double bed
          </p>
          </q-card-main>
         </q-card>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/room.jpg">
          </q-card-media>
          <q-card-title>
            10 Bed Dorm
          </q-card-title>
          <q-card-main>
          <p>R 160 pp</p>
          <p class="text-faded">
            For SAVAGES
          </p>
          </q-card-main>
         </q-card>
      </div>
      <div id="neightbours" class="row col-12">
        <div class="col-12"><div class="row justify-center"><H3> Neighbours On Long </H3></div></div>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/Beerhouse-outside-shot.jpg">
          </q-card-media>
          <q-card-title class="relative-position">
            <a href="https://www.google.com/maps/place/Beerhouse/@-33.9254393,18.4137894,17z/data=!3m1!4b1!4m5!3m4!1s0x1dcc676563828f1d:0xc6cee176ba5bc61d!8m2!3d-33.9254438!4d18.4159834">
              <q-btn fab color="primary" icon="place" class="absolute" style="top: 0; right: 8px; transform: translateY(-50%);" />
            </a>
            <a href="http://www.beerhouse.co.za/">Beer House</a>
          </q-card-title>
          <q-card-main>
          <p>BURP</p>
          <p class="text-faded">
            For the non sophisticated traveler that prefers to get drunk before getting laid.
          </p>
          </q-card-main>
         </q-card>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/room.jpg">
          </q-card-media>
          <q-card-title>
            Double Room
          </q-card-title>
          <q-card-main>
          <p>R 420</p>
          <p class="text-faded">
            For the sophisticated traveler that prefers privacy while getting
            laid on a double bed
          </p>
          </q-card-main>
         </q-card>
         <q-card class="col-sm-4 q-pa-sm">
          <q-card-media>
            <img src="statics/room.jpg">
          </q-card-media>
          <q-card-title>
            10 Bed Dorm
          </q-card-title>
          <q-card-main>
          <p>R 160 pp</p>
          <p class="text-faded">
            For SAVAGES
          </p>
          </q-card-main>
         </q-card>
      </div>
    </div>
  </q-page>
</template>

<style>

  img {
    max-width: 100%;
  }

  .vcent {
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

  .full {
    width: 100%;
    max-width: 1400px;
  }

</style>

<script>

export default {
  name: 'PageIndex'
}
</script>
