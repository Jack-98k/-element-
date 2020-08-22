<template>
  <div>
    <label v-if="lable">{{lable}}</label>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'LuoFormItem',
  props: {
    lable: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
</style>
