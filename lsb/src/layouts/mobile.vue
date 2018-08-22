<template>
  <q-page class="flex flex-center">
    <div  class="window-height window-width fill">
      <img src="statics/banner_pic.jpeg">
      </img>
    </div>

    <!-- BLURB -->
    <div id="blurb" class="row window-height window-width">
      <div class="col-3">
      </div>
      <div class="col-6 self-center">
        <div class="text-center">Long Street Backpackers is famous for its friendly and welcoming atmosphere, incredibly lush social spaces, communal activities, free meals and fantastic location. Set in a private oasis in the centre of Long Street there are literally thousands of eating, drinking and partying options right on your doorstep!</div>
      </div>
    </div>
    <!-- END BLURB -->

    <!-- LOCATION -->
    <div class="row window-height window-width">
      <div class="col-12">
        <H4> LOCATION </H4>
      </div>
      <iframe
          width="100%"
          height="100%"
          frameborder="0"
          style="border:0"
          src="https://www.google.com/maps/embed/v1/place?q=Long%20Street%20Backpackers%2C%20Long%20Street%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%20South%20Africa&key=AIzaSyDP2nBSjNH5WBMq9494cbbqOIroRtjxw-w"
          allowfullscreen>
        </iframe>
    </div>
    <div class="row window-height window-width">
      <div class="col-12">
        <H4> LOCATION </H4>
        <p> 209 Long Street, Cape Town</p>
      </div>
      <div class="col-12">
        <p> Centrally Located ...</p>
      </div>
      <div class="col-12">
        Walking distance to
      </div>
    </div>
    <!-- END LOCATION -->

    <q-parallax src="/statics/smaller_mobile.png" :height="500">
      <H1> DRINK UP </H1>
    </q-parallax>

      <!-- FACILITIES -->
    <div id="facilities" class="row window-height window-width justify-center q-pt-md items-start">
      <div class="row col-10">
        <div class="row col-4">
          <H4 class="q-mt-xl q-ml-lg"> FACILITIES </H4>
        </div>
      </div>
      <div class="row col-10">
        <div class="row col-8 q-pt-lg">
          <div class="col-4"><img width="60%" src="statics/icons/001-toast.svg"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/002-stove.svg"/></div>
          <div class="col-4"><img width="60%" src="statics/icons/003-lockers.svg"/></div>
        </div>
        <div class="row col-12 q-pt-lg">
          <div class="col-6 fill">
            <img src="/statics/bar.jpeg"></img>
          </div>
          <div class="col-6">

          </div>
        </div>
      </div>
    </div>
    <!-- END FACILITIES -->


  </q-page>
</template>

<style>

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

</style>

<script>
export default {
  name: 'mobile'
}
</script>
