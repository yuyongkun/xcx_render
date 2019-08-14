<template>
  <div class="container">
    <div class="login">
      <form>
        <div class="form-group">
          <input class="form-control" placeholder="用户名" />
        </div>
        <div class="form-group">
          <input class="form-control" placeholder="密码" />
        </div>
        <div class="form-group from-group-password">
          <a href="/modify_password">修改密码</a>
          <a href="/forget_password">忘记密码？</a>
        </div>
        <div class="form-group">
          <button class="binding-btn">确认绑定</button>
        </div>
      </form>
      <dl class="binding-tip">
        <dt>绑定须知：</dt>
        <dd>您现在是使用微信登录的</dd>
        <dd>您可以在此绑定原有TK账号</dd>
      </dl>
    </div>
  </div>
</template>
<style scoped lang="scss">
  .login{
    width:283px;
    margin:96px auto 0;
    font-size: 14px;
    .binding-btn{
      font-size: 14px;
      background-color: #5677FC;
      color:#fff;
    }
    .form-group{
      margin-bottom: 20px;
      .form-control{
        height: 38px;
        padding:0px 10px;
        border:1px solid #ddd;
        background-color: #fff;
      }
    }
    .from-group-password{
      text-align: right;
      a{
        display: inline-block;
        margin-right: 20px;
        color:#5578FC;
      }
    }
    .binding-tip{
      dt{
        margin-top: 60px;
        margin-bottom: 10px;
        color:#FF2A55;
      }
      dd{
        margin-left: 60px;
      }
    }
  }
</style>
