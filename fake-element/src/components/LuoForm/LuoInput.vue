<template>
  <div>
    <!-- 自定义组件双向绑定：:value @input -->
    <input :type="type" :value="value" @input="onInput" v-bind="$attrs" />
  </div>
</template>

<script>
export default {
  name: 'LuoInput',
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
      // 派发一个 input 事件
      this.$emit('input', e.target.value)
      // 通知父级执行校验
      this.$parent.$emit('validate')
    }
  }
}
</script>

<style scoped>
</style>
