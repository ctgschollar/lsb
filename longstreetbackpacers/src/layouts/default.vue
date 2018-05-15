<template>
  <q-layout view="hhh lpr FFF">
    <q-layout-header reveal :reveal-offset="0">
      <q-toolbar
        color="primary"
        :glossy="$q.theme === 'mat'"
        :inverted="$q.theme === 'ios'"
      >
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>

        <q-toolbar-title>
          Quasar App
          <div slot="subtitle">Running on Quasar v{{ $q.version }}</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-layout-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-layout-footer class="bg-primary">
      <form id="check_availability q-ma-md" action="https://hotels.cloudbeds.com/reservation/A9p5sR" method="post">
        <div class="container row justify-around">
          <q-datetime inverted class="q-pa" type="date" v-model="date" name="widget_date" id="date_1"/>
          <q-datetime inverted type="date" name="widget_date_to" v-model="dateTo" id="date_2"/>
          <input type="hidden" value="d/m/Y" name="date_format">
          <q-btn class="text-white bg-primary" type="submit" name="bf_submit" label="Check Availability"/>
          <!--<div class="q-title text-white vertical-middle"> BOOK NOW </div>-->
          <div class="clear_floats"></div>
        </div>
      </form>
    </q-layout-footer>
  </q-layout>
</template>

<script>
import { openURL, date } from 'quasar'

export default {
  name: 'LayoutDefault',
  data () {
    return {
      state: true,
      footer: true,
      header: true,
      date: new Date(),
      dateTo: date.addToDate(new Date(), { days: 1 })
    }
  },
  methods: {
    openURL
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
