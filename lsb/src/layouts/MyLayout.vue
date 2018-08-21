<template>
  <q-layout view="lHh Lpr lFf">
    <q-layout-header>
      HEADER
    </q-layout-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      desktop: this.$q.platform.is.desktop
    }
  },
  created() {
    if (this.desktop) {
        this.$router.push('/main');
    }
    else {
        this.$router.push('/mobile');
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>
</style>
