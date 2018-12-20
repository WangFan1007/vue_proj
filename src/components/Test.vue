<template>
  <div class="container">
    {{ msg }}
    <button @click="show = !show">Toggle</button>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated tada"
      leave-active-class="animated bounceOutRight"
    >
      <div class="main" v-if="show"></div>
    </transition>

    <el-button @click="visible = !visible">Button</el-button>
    <el-dialog :visible.sync="visible" title="Hello world">
      <p>Try Element</p>
    </el-dialog>
  </div>
</template>

<script>
import "animate.css";
// import { Toast } from "mint-ui";

export default {
  data: () => {
    return {
      msg: "hello World!",
      show: true,
      active: 1,
      visible: false
    };
  },
  methods: {}
};
</script>

<style scoped>
.main {
  width: 100%;
  height: 200px;
  background-color: rgb(56, 148, 14);
}

.container {
  /* background-color: #999; */
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>



