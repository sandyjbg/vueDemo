<template>
  <div>
    <el-alert
    title="错误提示的文案"
    type="error" v-if="flag" closable>
  </el-alert>
     <el-row>
        <el-col :span="24"><div class="grid-content bg-purple-dark1">
            <el-input v-model="input" placeholder="请输入账号（关大维2）"></el-input>
            <el-input v-model="input" placeholder="请输入密码"></el-input>
        </div></el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div class="grid-content bg-purple-dark2">
        <router-link to="budong/forgetpassword"><el-link type="primary">忘记密码</el-link></router-link></div></el-col>
    </el-row>
    <el-row>
         <el-col :span="24">
          <div class="grid-content bg-purple-dark2">
            <el-button type="primary" icon="el-icon-check" @click = "login">登录</el-button>
            <router-link to="budong/qnmykj">
              <el-button type="primary" icon="el-icon-plus">注册</el-button>
            </router-link>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
      return {
        input:"",
        flag :false
      }
    },
methods:{
  login(){
    this.flag = true;
  }
},
mounted() {

  }
}

</script>

<style>
.bg-purple-dark1{
  width: 250px;
  margin: 0 auto 25px auto;
}
.bg-purple-dark2{
  margin: 0 0 25px 0;
}
</style>
