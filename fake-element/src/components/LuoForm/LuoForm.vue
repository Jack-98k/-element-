<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'LuoForm',
  provide () {
    return {
      form: this
    }
  },
  props: {
    model: {
      type: Object,
      required: true
    },
    rules: {
      type: Object
    }
  }
}
</script>

<style scoped>
</style>
