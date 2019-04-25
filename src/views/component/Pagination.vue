<template>
  <div class="main">
    <el-button @click="search">刷新分页</el-button>
    <el-pagination
      @current-change="pagerChange"
      :current-page="pager.current"
      :page-size="10"
      layout="total, prev, pager, next, jumper"
      :total="pager.total"
      class="mt-20"
    ></el-pagination>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [],
      pager: {
        current: 1,
        total: 99
      }
    };
  },
  methods: {
    pagerChange(current) {},
    search() {
      // 总共的数据条数
      var total = Math.ceil(60 * Math.random());
      // 你的代码写下面
      this.pager.total = total;
    }
  }
};
</script>

<style scoped></style>