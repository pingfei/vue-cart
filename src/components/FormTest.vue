<template>
  <div class="">
    <h3>Element表单</h3>
    <hr>
    <el-form :model="model" :rules="rules" ref="loginForm">
      <el-form-item label="用户名" prop="username">
        <el-input v-model="model.username"></el-input>
      </el-form-item>
      
      <el-form-item label="密码" prop="password">
        <el-input v-model="model.password"></el-input>
      </el-form-item>

      <el-form-item>
        <el-button type="primary" @click="submitFrom('loginForm')">提交</el-button>
      </el-form-item>

    </el-form>

    <h2>KForm</h2>
    <hr>
    <k-input v-model="model.username"></k-input>
    <k-input type="password" v-model="model.username"></k-input>
  </div>
</template>
<script>
import KInput from '@/components/KInput.vue'
export default {
  components: {
    KInput
  },
  data () {
    return {
      model: {
        username: '',
        password: ''
      },
      rules: {
        username: [{required: true, message: '请输入用户名'}],
        password: [{required: true, message: '请输入密码'}]
      }
    }
  },
  methods: {
    submitFrom (form) {
      this.$refs[form].validate(valid => {
        if (valid) {
          alert('请求登录')
        } else {
          alert('校验失败')
        }
      })
    }
  }
}
</script>
<style scoped lang="">
</style>
