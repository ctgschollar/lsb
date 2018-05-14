<template>
  <q-page class="flex">
    <q-carousel :autoplay="5000" :infinite="true" height="100vh" class="full">
      <q-carousel-slide img-src="statics/room.jpg" w="500" />
      <q-carousel-slide img-src="statics/P4130376.jpg"/>
      <q-carousel-slide img-src="statics/P4130391.jpg"/>
    </q-carousel>
    <div class="container row justify-around full">
      <div class="col-sm-4">
        <div class="row justify-around">
          <div class="col-12"><img src="statics/code_of_arms_big.jpg" class="col-1"/></div>
          <div class="col-12">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean placerat ipsum in sapien bibendum, at lobortis ante tincidunt. Proin et quam sed ante tristique viverra. Suspendisse facilisis mauris luctus tellus pulvinar vehicula. Duis a viverra orci. Suspendisse lacinia ac tellus sit amet varius. Integer eu lobortis lectus, tempus facilisis massa. Quisque dictum vestibulum fermentum. Duis porta ligula sagittis egestas laoreet. Etiam pulvinar felis ut elit tristique scelerisque. Cras quis enim nisi. Quisque pellentesque molestie fermentum. Suspendisse ac nisi laoreet, fringilla mauris nec, congue nisi. Vivamus at neque ut justo molestie semper. Quisque nec urna sed tellus varius elementum. Fusce elementum mauris sit amet efficitur pellentesque. Aliquam sed commodo tortor.</div>
        <div>BRO</div>
        </div>
      </div>
      <div class="col-sm-8">
      <vue-instagram token="5450403056.d0833b5.9f78d8db81c5431488405ca186663590" username="christopherschollar" :count="5" :tags="['hashtag1', 'hashtag2']">
        <template slot="feeds" slot-scope="props">
          <li class="fancy-list"> {{ props.feed.link }} </li>
        </template>
        <template slot="error" slot-scope="props">
          <div class="fancy-alert"> {{ props.error.error_message }} </div>
        </template>
      </vue-instagram>
      </div>
    </div>
  </q-page>
</template>

<style>

  img {
    max-width: 100%;
  }

  .full {
    width: 100%;
    max-width: 1400px;
  }

</style>

<script>
export default {
  name: 'PageIndex',
  components : {
    VueInstagram
  }
}
</script>
