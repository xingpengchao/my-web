<template>
  <div class="index">
    <el-row>
      <el-button>Default</el-button>
      <el-button class="custom" type="primary" @click="goTarget(url)">Primary</el-button>
      <el-button type="success">Success</el-button>
      <el-button type="info">Info</el-button>
      <el-button type="warning">Warning</el-button>
      <el-button type="danger">Danger</el-button>
    </el-row>
  </div>
</template>

<script setup name="Index">
const url = ref('http://www.baidu.com')

function goTarget(url) {
  window.open(url, '__blank')
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables.module.scss";

.index {
  background: #ffffff;
  min-height: 100vh;
  .custom {
    height: px2vh(120);
    width: px2vw(200);
  }
}
</style>

