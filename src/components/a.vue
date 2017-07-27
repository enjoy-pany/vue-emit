<template>
  <div class="adiv">
    <p>a组件</p>
    <button type="button" v-on:click="handleClick">点击打开组件b弹窗</button>
  </div>
</template>

<script>

export default {
  methods: {
    handleClick () {
      this.$emit('isLogFn','log')
    }
  }
}
</script>

<style>
.adiv{
  width: 400px;
  height: 200px;
  border: 1px solid #000;
  margin: 0 auto;
}
</style>
