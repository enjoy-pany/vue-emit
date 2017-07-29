<template>
  <div class="bdiv">
    我是组件B弹窗{{isLogin}}
    <button type="button" @click='close'>点击关闭</button>
  </div>
</template>

<script>
export default {
  props: ['isLog'],
  data () {
    return {

    }
  },
  methods: {
    close () {
      this.$emit('isLogFn','close')
    }
  },
  computed: {
    isLogin () {
      return this.isLog
    }
  },
  created () {
    console.log('b组件被created')
    console.log('b组件拿到了 ID = ' + this.isLogin + '开始发送ajax啦^_^')
  },
  mounted () {
    console.log('b组件被mounted')
  },
  updated () {
    console.log('b组件被updated')
  },
  destroyed () {
    console.log('关闭弹窗之后，b组件被destroyed ~_~')
  }
}
</script>

<style>
  .bdiv{
    width: 200px;
    height: 200px;
    border: 1px #000 solid;
    margin: 0 auto;
    text-align: center;
  }
  .bdiv button {
    display: block;
    margin: 50px auto
  }

</style>
