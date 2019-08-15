
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
    <TaskList :qtype="qtype" />
  </div>
</template>
<script>
import TaskList from "../../components/tasklist.vue";
export default {
  data() {
    return {
      num: 1,
      qtype: 0
    };
  },
  components: {
    TaskList: TaskList
  },
  methods: {
    tabOpt(index) {
      this.num = index;
      this.qtype = this.num;
    }
  }
};
</script>
