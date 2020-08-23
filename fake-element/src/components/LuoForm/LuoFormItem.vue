<template>
  <div>
    <label v-if="lable">{{lable}}</label>
    <slot></slot>
    <!-- 校验信息显示 -->
    <p v-if="error">{{error}}</p>
  </div>
</template>

<script>
import Schema from 'async-validator'
export default {
  inject: ['form'],
  name: 'LuoFormItem',
  props: {
    lable: {
      type: String,
      default: ''
    },
    prop: {
      type: String
    }
  },
  data () {
    return {
      error: ''
    }
  },
  mounted () {
    this.$on('validate', function () {
      this.validate()
    })
  },
  methods: {
    validate () {
      // 规则
      const rules = this.form.rules[this.prop]
      // 当前值
      const value = this.form.model[this.prop]
      // 校验描述对象
      const desc = {
        [this.prop]: rules
      }
      // 创建Schema实例
      const schema = new Schema(desc)
      schema.validate({ [this.prop]: value }, errors => {
        if (errors) {
          this.error = errors[0].message
        } else {
          // 校验通过
          this.error = ''
        }
      })
    }
  }
}
</script>

<style scoped>
</style>
