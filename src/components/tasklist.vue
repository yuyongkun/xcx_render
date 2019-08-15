<template>
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
</template>
<script>
export default {
  props: ["qtype"],
  data() {
    return {
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
  mounted() {
    // this.queryTaskList();
  },
  methods: {
    queryTaskList() {
      wx.request({
        url: "/",
        data: {
          type: this.qtype
        },
        header: {
          "content-type": "application/json" // 默认值
        },
        success: function(res) {
          this.list = res.data;
        }
      });
    }
  },
  watch: {
    qtype(newVal, oldVal) {
      this.qtype = newVal;
      this.queryTaskList();
    }
  }
};
</script>