<template>
  <div class="main">
    选择水果(单选):
    <el-select v-model="value" placeholder="请选择">
      <el-option v-for="item in list" :key="item.value" :label="item.label" :value="item.value"></el-option>
    </el-select>
    选择水果(多选):
    <el-select v-model="valueArr" multiple placeholder="请选择">
      <el-option v-for="item in list" :key="item.value" :label="item.label" :value="item.value"></el-option>
    </el-select>
    用户数据(远程数据):
    <el-select v-model="userValue" placeholder="请选择">
      <el-option v-for="item in remoteList" :key="item.id" :label="item.name" :value="item.id"></el-option>
    </el-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          label: "苹果",
          value: 1
        },
        {
          label: "梨",
          value: 2
        },
        {
          label: "香蕉",
          value: 3
        },
        {
          label: "荔枝",
          value: 4
        }
      ],
      value: "",
      userValue: "",
      valueArr: [],
      remoteList: []
    };
  },
  methods: {
    fetchRemoteList() {
      this.$http
        .get("https://jsonplaceholder.typicode.com/users")
        .then(data => {
          // 你的代码在这里
          this.remoteList = data.data;
        });
    }
  },
  mounted() {
    this.fetchRemoteList();
  }
};
</script>

<style scoped></style>