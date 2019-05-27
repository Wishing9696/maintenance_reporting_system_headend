<template>
  <div>
    <div class="head">
      <span>
        <b>HANSONG</b>
      </span>
    </div>
    <el-divider></el-divider>
    <el-row class="menu">
      <el-col class="menu-col" :span="3">
        <el-menu
          router
          class="select-menu"
          default-active="/"

        >
          <el-menu-item index="/upload">维修上传</el-menu-item>
          <el-menu-item index="/table">报表</el-menu-item>
        </el-menu>
      </el-col>
      <el-col class="body-col" :span="21">
        <el-card style="margin-left:10px">
          <router-view/>
        </el-card>
      </el-col>
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

<style>
.head {
  margin-left: 10px;
  letter-spacing: 1px;
  font-size: 30px;
  color: red;
}
.el-col {
  height: 100%;
}
</style>
