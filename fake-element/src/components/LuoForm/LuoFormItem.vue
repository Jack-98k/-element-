<template>
  <div>
    <label v-if="lable">{{lable}}</label>
    <slot></slot>
    <!-- 校验信息显示 -->
    <p v-if="error">{{error}}</p>
  </div>
</template>

<script>
export default {
  inject: ['form'],
  name: 'LuoFormItem',
  props: {
    lable: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      error: ''
    }
  }
}
</script>

<style scoped>
</style>
