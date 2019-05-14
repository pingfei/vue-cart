<template>
  <div class="">
    <input :type="type" :value="value" @input="onInput">
  </div>
</template>
<script>
export default {
  data () {
    return {}
  },
  props: {
    value: {
      type: String,
      default: ''
    },
    type: {
      type: String,
      default: 'text'
    }
  },
  methods: {
    onInput (e) {
      // 派发事件，通知父组件输入值的变化
      this.$emit('input', e.target.value)
    }
  }
}
</script>
<style scoped lang="">
</style>
