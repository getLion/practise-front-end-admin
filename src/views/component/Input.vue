<template>
  <div class="main">
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-input type="textarea" :rows="2" placeholder="请输入内容" v-model="textarea"></el-input>
    <el-input type="number" v-model="num" placeholder="请输入数字"></el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      textarea: "",
      num: ""
    };
  },
  methods: {}
};
</script>

<style>
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}
input[type="number"] {
  -moz-appearance: textfield;
}
</style>