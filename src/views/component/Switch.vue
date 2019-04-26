<template>
  <div class="main">
    <el-switch v-model="value" on-text="开" off-text="关"></el-switch>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: true
    };
  },
  methods: {}
};
</script>

<style scoped></style>