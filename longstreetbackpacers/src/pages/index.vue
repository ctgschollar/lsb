<template>
  <q-page class="flex">
    <q-carousel :autoplay="5000" :infinite="true" height="100vh" class="full">
      <q-carousel-slide img-src="statics/room.jpg" w="500" />
      <q-carousel-slide img-src="statics/P4130376.jpg"/>
      <q-carousel-slide img-src="statics/P4130391.jpg"/>
    </q-carousel>
    <div class="container row justify-around full">
      <div class="col-sm-5">
        <div class="row justify-center">
          <div class="col-12"><img src="statics/code_of_arms_big.jpg" class="col-1"/></div>
          <div class="col-12 q-px-lg" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean placerat ipsum in sapien bibendum, at lobortis ante tincidunt. Proin et quam sed ante tristique viverra. Suspendisse facilisis mauris luctus tellus pulvinar vehicula. Duis a viverra orci. Suspendisse lacinia ac tellus sit amet varius. Integer eu lobortis lectus, tempus facilisis massa. Quisque dictum vestibulum fermentum. Duis porta ligula sagittis egestas laoreet. Etiam pulvinar felis ut elit tristique scelerisque. Cras quis enim nisi. Quisque pellentesque molestie fermentum. Suspendisse ac nisi laoreet, fringilla mauris nec, congue nisi. Vivamus at neque ut justo molestie semper. Quisque nec urna sed tellus varius elementum. Fusce elementum mauris sit amet efficitur pellentesque. Aliquam sed commodo tortor.</div>
          <div class="col-12 row justify-center"><H3>Facilities</H3></div>
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
