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
        <div class="form-group">
          <router-link to="/foo">修改密码</router-link>
          <router-link to="/foo">忘记密码？</router-link>
        </div>
        <div class="form-group">
          <button class="button">确认绑定</button>
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
