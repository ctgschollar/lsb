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

    <q-layout-footer >
      <form id="check_availability" action="https://hotels.cloudbeds.com/booking/reservation/R43szk" method="post">
          <p class="col_25 date_input"><input name="widget_date" type="text" maxlength="10" value="13/05/2018" class="datepicker_input hasDatepicker" id="date_1"></p>
          <p class="col_25 date_input"><input name="widget_date_to" type="text" maxlength="10" value="16/05/2018" class="datepicker_input hasDatepicker" id="date_2"></p>
          <p class="col_25">
              <input type="hidden" value="d/m/Y" name="date_format">
              <button type="submit" name="bf_submit" onclick="_gaq.push(['_trackEvent', 'Check Availability', 'Submit']);">Check Availability</button>
          </p>
          <p class="col_25" id="price_guarantee"><span>Best price guaranteed!</span></p>
          <div class="clear_floats"></div>
      </form>
    </q-layout-footer>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'LayoutDefault',
  data () {
    return {
      state: true,
      footer: true,
      header: true
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>

</style>
