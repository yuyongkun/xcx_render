
<template>
  <div class="container">
    <div class="search">
      <div class="search-nav">
        <input
          class="form-control"
          v-model="keyworkd"
          @keyup.enter="searchOpt"
          type="text"
          placeholder="输入任务号"
        />
        <img @click="searchOpt" class="search-icon" src="/static/images/search-icon.png" />
      </div>
    </div>
    <div class="search-mask"></div>
    <div class="task-list">
      <template v-if="list.length>0">
        <div v-for="item in list" :key="item" class="task-item">
          <img class="task-cover" src="/static/images/no-task-bg.png" />
          <div class="task-desc">
            <div class="task-number">{{item.taskNumber}}</div>
            <div class="task-name">{{item.taskName}}</div>
            <div class="task-price">{{item.taskPrice}}</div>
            <div class="task-status">{{item.taskStatus}}</div>
          </div>
        </div>
      </template>
      <template v-else>
        <div class="no-task-icon">
          <img src="/static/images/no-task-bg.png" />
          没有您的任务
          <br />快去渲染吧~
          <div class="no-task-warning">
            <p>
              <em>没找到您的任务吗？</em>
            </p>
            <p>请检查当前账号，或联系客服。</p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<style scoped lang="scss">
.search {
  width: 100%;
  font-size: 14px;
  position: relative;
  z-index: 2;
  .search-nav {
    position: relative;
    padding: 18px 24px 26px;
    background-color: #fff;
  }
  .form-control {
    height: 38px;
    padding: 0px 20px;
    border: 1px solid #ddd;
    border-radius: 19px;
    background-color: #fff;
  }
  .search-nav .search-icon {
    position: absolute;
    width: 38px;
    height: 38px;
    right: 40px;
    top: 20px;
    padding: 10px;
    z-index: 2;
    box-sizing: border-box;
  }
}
.search-mask {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.7);
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 1;
}
</style>
<script>
export default {
  data() {
    return {
      keyworkd: "",
      list: [
        {
          taskNumber: "658109",
          taskName: "室内渲染.max",
          taskPrice: "10.00",
          taskStatus: "待结算"
        },
        {
          taskNumber: "658109",
          taskName: "室内渲染.max",
          taskPrice: "10.00",
          taskStatus: "待结算"
        },
        {
          taskNumber: "658109",
          taskName: "室内渲染.max",
          taskPrice: "10.00",
          taskStatus: "待结算"
        }
      ]
    };
  },
  methods: {
    searchOpt() {
      let arr = [
        {
          taskNumber: "258109",
          taskName: "建筑渲染.max",
          taskPrice: "20.00",
          taskStatus: "待结算"
        }
      ];
      this.list = arr;
      //   wx.request({
      //     url: "/",
      //     data: {
      //       keyworld: this.keyworkd
      //     },
      //     header: {
      //       "content-type": "application/json" // 默认值
      //     },
      //     success: function(res) {
      //       this.searchFlag = true;
      //       let arr = [
      //         {
      //           taskNumber: "258109",
      //           taskName: "建筑渲染.max",
      //           taskPrice: "20.00",
      //           taskStatus: "待结算"
      //         }
      //       ];
      //       this.list = res.data;
      //     }
      //   });
    }
  }
};
</script>