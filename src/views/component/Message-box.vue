<template>
  <div class="main">
    <el-button type="danger" @click="open">删除</el-button>
    <br>
    姓名: {{name}}
    <el-button :plain="true" @click="open2">录入姓名</el-button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "未设置"
    };
  },
  methods: {
    open() {
      this.$confirm("确定删除？", "提示", {
        confirmButtonText: "确定",
        cancelButtonText: "取消",
        type: "warning"
      })
        .then(() => {
          this.name = "未设置"
          this.$message({
            type: "success",
            message: "删除成功!"
          });
        })
        .catch(() => {
          this.$message({
            type: "info",
            message: "已取消删除"
          });
        });
    },
    open2() {
        this.$prompt('请输入姓名', '提示', {
          confirmButtonText: '确定',
          cancelButtonText: '取消'
        }).then(({ value }) => {
          this.name= value
        }).catch(() => {
          this.$message({
            type: 'info',
            message: '取消输入'
          });       
        });
      }
  },
  mounted() {
    this.$message("本网站基于 Vue 开发");
  }
};
</script>

<style scoped></style>