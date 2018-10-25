<template>
  <div>
    <div class="sign">
      <div class="logo">
        <img style= "width: 100%;vertical-align: center" src="//cdn2.jianshu.io/assets/web/logo-58fd04f6f0de908401aa561cda6a0688.png">
      </div>
      <div class="main">
        <b-card no-body>
          <b-tabs pills card>
            <b-tab title="登录" class="title">
              <form>
                <input style="margin-bottom: 0;position: relative;width: 100%;" placeholder="手机号或邮箱" v-model="email"/>
                <input  style="margin-bottom: 0;position: relative;width: 100%;"placeholder="密码" v-model="password"/>
              </form>
              <div style="float:left;margin: 15px 0">
                <input type="checkbox"/>
                <span>记住我</span>
              </div>
              <div class="forget-btn">
                <a>登录遇到的问题</a>
              </div>
              <el-button  class="sign-in-button" type="primary" plain @click="onClick">登录</el-button>
              <div class="more-sign">
                <h6>更多账号登录</h6>
              </div>
            </b-tab>
            <b-tab title="注册" class="title">
              <form>
                <input style="margin-bottom: 0;position: relative;width: 100%;" placeholder="你的账号"/>
                <input  style="margin-bottom: 0;position: relative;width: 100%;"placeholder="手机号"/>
                <input  style="margin-bottom: 0;position: relative;width: 100%;"placeholder="设置密码"/>
              </form>
              <el-button  class="sign-in-button" type="primary" plain>注册</el-button>
              <p class="sign-up-msg">点击 “注册” 即表示您同意并愿意遵守简书</p>
              <a href="http://www.jianshu.com/p/c44d171298ce">用户协议</a>和<a href="http://www.jianshu.com/p/2ov8x3">隐私政策</a>
              <div class="more-sign">
                <h6>社交账号直接注册</h6>
              </div>
            </b-tab>
          </b-tabs>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Login",
      methods: {
        onClick() {
          var that = this;
          this.$http
            .post('http://localhost:8080/user/sign_in', {"email": this.email, "password": this.password})
            .then(function (response) {
              alert(JSON.stringify(response.data.data));
              localStorage.setItem("loginUser", JSON.stringify(response.data.data))
              that.$router.push("/")
            })
        }
      }
    }
</script>

<style scoped>
  .sign-up-msg{
    margin: 10px 0;
    padding: 0;
    text-align: center;
    font-size: 12px;
    line-height: 20px;
    color: #969696;
  }
  .more-sign{
    position: relative;
    margin: 0 0 10px;
    font-size: 12px;
    color: #b5b5b5;
  }
  .sign-in-button{
    margin-top: 20px;
    width: 100%;
    padding: 9px 18px;
    font-size: 18px;
    border: none;
    border-radius: 25px;
    color: #fff;
    cursor: pointer;
    outline: none;
    display: block;
    clear: both;
  }
  .forget-btn{
    float: right;
    position: relative;
    margin: 15px 0;
    font-size: 14px;
  }
  .title{
    margin: 0 auto 50px;
    padding: 10px;
    font-weight: 400;
    color: #969696;
  }
  .main{
    width: 400px;
    margin: 60px auto 0;
    padding: 50px 50px 30px;
    background-color: #fff;
    border-radius: 4px;
    box-shadow: 0 0 8px rgba(0,0,0,.1);
    vertical-align: middle;
    display: inline-block;
  }
  .logo{
    position: absolute;
    top: 56px;
    margin-left: 50px;
  }
.sign{
  height: 100%;
  min-height: 750px;
  text-align: center;
  font-size: 14px;
  background-color: #f1f1f1;
}
</style>
