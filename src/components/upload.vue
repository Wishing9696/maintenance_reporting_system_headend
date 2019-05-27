<template>
  <el-card class="box-card">
    <div slot="header">
      <span>
        <b>维修上传</b>
      </span>
      <el-button type="primary" @click="dialogVisible = true" style="margin-left:20px">新增维修记录</el-button>
    </div>
    <div></div>
    <el-dialog title="提示" :visible.sync="dialogVisible" width="30%" :before-close="handleClose">
      <span>这是一段信息</span>
      <span slot="footer" class="dialog-footer">
        <el-button @click="handlecancel">取 消</el-button>
        <el-button type="primary" @click="handlesave">确 定</el-button>
      </span>
    </el-dialog>
  </el-card>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false
    };
  },
  methods: {
    handleClose(done) {
      this.$confirm("确认关闭？")
        .then(_ => {
          done();
        })
        .catch(_ => {});
    },
    handlecancel() {
      this.dialogVisible = false;
    },
    handlesave() {
      this.dialogVisible = false;
    }
  }
};
</script>