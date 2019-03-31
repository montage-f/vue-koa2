/**Created by MonTage_fz on 2019/3/31**/
<template>
  <div class="Register">
    <div class="header">
      <div class="header-content">
        <div class="logo"></div>
        <div class="signIn">
          <span>已有美团账号?</span>
          <span>登录</span>
        </div>
      </div>
    </div>
    <div class="content">
      <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
        <el-form-item label="账号" prop="name">
          <el-input v-model="ruleForm.name" class="maxWidth"></el-input>
        </el-form-item>
        <el-form-item label="请输入邮箱" prop="email">
          <div class="phone">
            <el-input v-model="ruleForm.email" class="maxWidth"></el-input>
            <span>注册成功后，全美团通用</span>
          </div>
          <button>免费获取短信动态码</button>
        </el-form-item>
        <el-form-item label="短信动态码" prop="code">
          <el-input v-model="ruleForm.code" class="maxWidth"></el-input>
        </el-form-item>
        <el-form-item label="创建密码" prop="password">
          <el-input v-model="ruleForm.password" class="maxWidth"></el-input>
        </el-form-item>
        <el-form-item label="确认密码" prop="surePassword">
          <el-input v-model="ruleForm.surePassword" class="maxWidth"></el-input>
        </el-form-item>
      </el-form>
      <div class="footer">
        <p class="button">
          <button>同意以下协议并注册</button>
        </p>
        <p>《美团网用户协议》</p>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'Register',
    layout: 'BlackTemplate',
    components: {},
    data() {
      let validatePass2 = (rule, value, callback) => {
        if (value === '') {
          callback(new Error('请再次输入密码'))
        } else if (value !== this.ruleForm.password) {
          callback(new Error('两次输入密码不一致!'))
        } else {
          callback()
        }
      }
      return {
        ruleForm: {
          name: '',
          code: '',
          email: '',
          password: '',
          surePassword: ''
        },
        rules: {
          name: [
            { required: true, message: '请输入昵称', trigger: 'blur' }
          ],
          email: [
            { required: true, message: '请输入邮箱地址', trigger: 'blur' },
            { type: 'email', message: '请输入正确的邮箱地址', trigger: ['blur', 'change'] }
          ],
          code: [
            { required: true, message: '请输入验证码', trigger: 'blur' }
          ],
          password: [
            { required: true, message: '创建密码', trigger: 'blur' }
          ],
          surePassword: [
            { required: true, message: '确认密码', trigger: 'blur' },
            {
              validator: validatePass2, trigger: 'blur'
            }
          ]
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
  .Register {
    width: 100%;
    .header {
      border-bottom: 2px solid #2bb8aa;
      .header-content {
        height: 60px;
        max-width: 980px;
        margin: 0 auto;
        padding: 10px 0;
        box-sizing: border-box;
        display: flex;
        justify-content: space-between;
        .logo {
          width: 54px;
          height: 100%;
          background: url('../assets/img/sprite.png') no-repeat -669px -748px;
        }
        .signIn {
          color: #666666;
          font-size: 14px;
          display: flex;
          align-items: center;
          span {
            margin-right: 20px;
            &:nth-last-of-type(1) {
              &:hover {
                cursor: pointer;
              }
              width: 46px;
              height: 24px;
              color: #fff;
              background-image: linear-gradient(to bottom, #2ec3b4, #2db3a6);
              text-align: center;
              font-size: 12px;
              line-height: 24px;
              margin: 0;
            }
          }
        }
      }

    }
    .content {
      box-sizing: border-box;
      max-width: 980px;
      margin: 38px auto 0;
      .maxWidth {
        display: flex;
        width: 260px;
      }
      .phone {
        display: flex;
        font-size: 12px;
        color: #999999;
        .maxWidth {
          margin-right: 20px;
        }
      }
      .footer {
        padding-left: 100px;
        p {
          height: 36px;
          box-sizing: border-box;
          line-height: 33px;
          &:nth-last-of-type(1) {
            color: #2ebcae;
          }
        }
        .button {
          button {
            padding: 10px 20px;
            background: #2ebcae;
            color: #fff;
            font-weight: bold;
            border: 0;
          }
        }
      }
    }
  }
</style>
