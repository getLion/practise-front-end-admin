<template>
  <div class="main">
    <el-table :data="list" border align="center" stripe>
      <el-table-column type="index" label="序列" align="center" width="80"></el-table-column>
      <el-table-column prop="name" label="姓名"></el-table-column>
      <el-table-column prop="gender" label="性别" :formatter="formatSex"></el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          name: "Joel",
          gender: 1
        },
        {
          name: "Mary",
          gender: 2
        },
        {
          name: "Jimmy",
          gender: 3
        }
      ]
    };
  },
  methods: {
    formatSex: function(row, column) {
      if (row.gender === 1) {
        return "男";
      } else if (row.gender === 2) {
        return "女";
      } else {
        return "未知";
      }
    }
  }
};
</script>

<style scoped></style>