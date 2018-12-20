<template>
  <div class="container">
    <el-header>
      <el-row>
        <el-col :span="12">
          <el-steps :active="active" class="steps" align-center>
            <el-step title="Setup"></el-step>
            <el-step title="Business"></el-step>
            <el-step title="Vehicle"></el-step>
            <el-step title="Finish"></el-step>
          </el-steps>
        </el-col>
        <el-col :span="1" :offset="10">
          <el-button plain id="skip">skip</el-button>
        </el-col>
      </el-row>
    </el-header>

    <el-footer>
      <el-button style="margin-top: 12px;" @click="next">下一步</el-button>
    </el-footer>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      visible: true,
      active: 0
    };
  },
  methods: {
    next() {
      if (this.active++ > 3) this.active = 0;
    }
  }
};
</script>

<style scoped>
.container {
  width: 90%;
  height: 90%;
  margin-top: 2.5%;
  margin-left: 5%;
  background-color: #fff;
  position: fixed;
  border-radius: 5px;
}

.el-header {
  text-align: center;
  margin-top: 20px;
}
#skip {
  border-width: 0;
}
</style>


