/**Created by MonTage_fz on 2019/3/31**/
<template>
  <div class="Login">
    <div class="content">
      <div class="message">
        <div class="img"></div>
        <div class="info"></div>
      </div>
      <div class="signIn">
        <el-form :model="ruleForm" :rules="rules" ref="ruleForm" class="demo-ruleForm">
          <el-form-item prop="name">
            <el-input v-model="ruleForm.name" placeholder="手机号/用户名/邮箱"></el-input>
          </el-form-item>
          <el-form-item prop="password">
            <el-input v-model="ruleForm.password" placeholder="密码"></el-input>
          </el-form-item>
        </el-form>
        <el-button>登录</el-button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Login',
    layout: 'BlackTemplate',
    components: {},
    data() {
      return {
        ruleForm: {
          name: '',
          password: ''
        }
      }
    },
    created() {
    },
    computed: {},
    methods: {}
  }
</script>

<style scoped lang="less">
  .Login {
    padding-top: 40px;
    .content {
      max-width: 865px;
      margin: 0 auto;
      display: flex;
      .message {
        flex: 1;
        .img {
          width: 82px;
          height: 54px;
          background: url('../assets/img/sprite.png') no-repeat -188px -808px;
        }
      }
      .signIn {
        width: 270px;
        padding-top: 72px;
      }
    }
  }
</style>
