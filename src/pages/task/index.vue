
<template>
  <div class="container">
    <div class="tab">
      <div class="tab-item" :class="{active:num==1}" @click="tabOpt(1)">
        <span>进行中(2)</span>
      </div>
      <div class="tab-item" :class="{active:num==2}" @click="tabOpt(2)">
        <span>已完成(3/5)</span>
        <div class="tab-radio-tip"></div>
      </div>
    </div>
    <div class="task-list">
      <template v-if="hasTask">
        <div class="task-item">
          <img class="task-cover" src="/static/images/no-task-bg.png" />
          <div class="task-desc">
            <div class="task-number">658109</div>
            <div class="task-name">室内渲染.max</div>
            <div class="task-price">10.00</div>
            <div class="task-status">待结算</div>
          </div>
        </div>
        <div class="task-item">
          <img class="task-cover" src="/static/images/no-task-bg.png" />
          <div class="task-desc">
            <div class="task-number">658109</div>
            <div class="task-name">室内渲染.max</div>
            <div class="task-price">10.00</div>
            <div class="task-status">待结算</div>
          </div>
        </div>
        <div class="task-item">
          <img class="task-cover" src="/static/images/no-task-bg.png" />
          <div class="task-desc">
            <div class="task-number">658109</div>
            <div class="task-name">室内渲染.max</div>
            <div class="task-price">10.00</div>
            <div class="task-status">待结算</div>
          </div>
        </div>
      </template>
      <template v-if="!hasTask">
        <div class="no-task-icon">
          <img src="/static/images/no-task-bg.png" />
          没有您的任务<br/>快去渲染吧~
          <div class="no-task-warning">
              <p><em>没找到您的任务吗？</em></p>
              <p>请检查当前账号，或联系客服。</p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      num: 1,
      hasTask: true
    }
  },

  methods: {
    tabOpt(index) {
      this.num = index
    }
  }
}
</script>
