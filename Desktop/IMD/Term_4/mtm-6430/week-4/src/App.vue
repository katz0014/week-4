<template>
  <div id="app">
    <el-button type="primary" @click="openDiag = true">Welcome</el-button>
    <el-dialog :visible.sync="openDiag">
      <div>
        <input type="text" v-model="newLaptop" />
      </div>
      <HelloWorld msg="My first try at making an app" />
      <FirstTry :treat="newLaptop" />
    </el-dialog>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import FirstTry from "./components/FirstTry.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    FirstTry
  },
  data: function() {
    return {
      newLaptop: "chicken fingers and fries",
      openDiag: false
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
