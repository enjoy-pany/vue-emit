<template>
  <div id="app">
    <aPage @isLogFn = "lisLogFn"></aPage>
    <bPage @isLogFn = "lisLogFn" :isLog = "id" v-if="login"></bPage>
  </div>
</template>

<script>

import aPage from './components/a.vue'
//const aPage = resolve => require(['./components/a.vue'], resolve)
import bPage from './components/b.vue'
//const bPage = resolve => require(['./components/b.vue'], resolve)

export default {
  data () {
    return {
      id: 1,
      login: false
    }
  },
  name: 'app',
  components: {
    aPage,
    bPage
  },
  methods: {
    lisLogFn (data) {
      if (data == 'open') {
        this.login = true
      } else if (data == 'close') {
        this.login = false
      }
    }
  },
  created () {
    console.log('父组件被created')
  },
  mounted () {
    console.log('父组件被mounted')
  },
  updated () {
    console.log('父组件被updated')
  },
  destroyed () {
    console.log('父组件被destroyed')
  }
}
</script>

<style>
</style>
