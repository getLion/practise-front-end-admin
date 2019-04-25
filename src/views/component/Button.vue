<template>
  <div class="main">
    <el-row>
      <el-button type="success">成功按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
      <el-button type="info">信息按钮</el-button>
    </el-row>
    <el-row>
      <el-button>默认按钮</el-button>
      <el-button size="medium">中等按钮</el-button>
      <el-button size="small">小型按钮</el-button>
    </el-row>
    <el-row>
      <el-button type="text">文字按钮</el-button>
    </el-row>
    <el-row>
      <el-button disabled>禁用按钮</el-button>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {}
};
</script>

<style scoped>
</style>