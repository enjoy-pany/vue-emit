<template>
  <div id="app">
    <aPage @isLogFn = "lisLogFn"></aPage>
    <bPage :isLog = "login"></bPage>
  </div>
</template>

<script>

import aPage from './components/a.vue'
import bPage from './components/b.vue'

export default {
  data () {
    return {
      login: 'false'
    }
  },
  name: 'app',
  components: {
    aPage,
    bPage
  },
  methods: {
    lisLogFn (data) {
      if (data == 'log') {
        this.login = 'true'
      }
    }
  }
}
</script>

<style>
</style>
