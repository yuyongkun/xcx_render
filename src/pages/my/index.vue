<template>
  <div class="container">
    <div class="my">
      <div class="my-head">
        <div class="my-head-user">
          <div class="my-head-portrait">
            <img src="/static/images/my-icon.png" />
          </div>

          <div class="my-head-rt">
            <h3>shz</h3>
            <p>渲染用户</p>
          </div>
        </div>
        <div class="my-head-account">
          <dl>
            <dt>66.66</dt>
            <dd>渲染币</dd>
          </dl>
          <dl>
            <dt>66.66</dt>
            <dd>金币</dd>
          </dl>
          <dl>
            <dt>66.66</dt>
            <dd>渲染券</dd>
          </dl>
        </div>
      </div>
      <div class="my-content">
        <div class="activity-banner">
          <a href="#">点击查看 →</a>
        </div>
        <h3>V5CG云渲染共帮您节省了1000元</h3>
        <ul>
          <li>
            <img src="/static/images/invite-icon.png" />
            邀请好友
            <img class="arrow-right" src="/static/images/arrow-right-icon.png" />
          </li>
          <li>
            <img src="/static/images/user-account-bind-icon.png" />
            绑定账号
            <img class="arrow-right" src="/static/images/arrow-right-icon.png" />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>
<style scoped lang="scss">
.my {
  width: 100%;
  font-size: 14px;
  .my-head {
    .my-head-user {
      display: flex;
      padding: 40px 24px;
      background-color: #333;
      .my-head-portrait {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: #fff;
        overflow: hidden;
        img {
          display: block;
          width: 100%;
          height: 100%;
        }
      }
      .my-head-rt {
        flex: 1;
        padding: 0 24px;
        h3 {
          margin-bottom: 3px;
          font-weight: normal;
          font-size: 18px;
          color: #fff;
        }
        p {
          color: rgba(255, 255, 255, 0.75);
        }
      }
    }
    .my-head-account {
      display: flex;
      justify-content: center;
      padding: 10px 0px;
      border-bottom: 1px solid #ddd;
      background-color: rgba(255, 255, 255, 0.9);
      dl {
        flex: 1;
        text-align: center;
        dt {
          margin-bottom: 10px;
          font-size: 14px;
        }
        dd {
          font-size: 12px;
        }
      }
    }
  }
  .my-content {
    padding: 10px 24px;
    .activity-banner {
      display: flex;
      width: 335px;
      height: 50px;
      align-items: center;
      justify-content: flex-end;
      margin: 0 auto 15px;
      border-radius: 4px;
      text-align: right;
      background-color: #f7dc97;
      a {
        margin-right: 10px;
        font-size: 12px;
        color: #5b533c;
      }
    }
    h3 {
      margin-bottom: 26px;
      text-align: center;
      color: #5677fc;
    }
    ul {
      li {
        margin-bottom: 20px;
        font-size: 14px;
        img {
          width: 20px;
          height: 20px;
          margin-right: 15px;
          vertical-align: middle;
        }
        .arrow-right {
          float: right;
          width: 20px;
          height: 20px;
          padding: 5px;
          box-sizing: border-box;
        }
      }
    }
  }
}
</style>