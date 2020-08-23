<template>
  <div>
    <LuoForm :model="userInfo" :rules="rules">
      <LuoFormItem lable="用户名">
        <LuoInput v-model="userInfo.username"></LuoInput>
      </LuoFormItem>
      <LuoFormItem lable="密码">
        <LuoInput type="password" v-model="userInfo.password"></LuoInput>
      </LuoFormItem>
    </LuoForm>
  </div>
</template>

<script>
import LuoInput from '@/components/LuoForm/LuoInput.vue'
import LuoFormItem from '@/components/LuoForm/LuoFormItem.vue'
import LuoForm from '@/components/LuoForm/LuoForm.vue'

export default {
  name: 'LuoFormExample',
  components: {
    LuoInput,
    LuoFormItem,
    LuoForm
  },
  data () {
    return {
      userInfo: {
        username: '',
        password: ''
      },
      rules: {
        username: [{ required: true, message: '请输入用户名称' }],
        password: [{ required: true, message: '请输入密码' }]
      }
    }
  }
}
</script>

<style scoped>
</style>
