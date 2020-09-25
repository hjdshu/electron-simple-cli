<template>
  <div id="app">
    <button @click="copy">复制下面这段字</button>
    <input type="text" v-model="val">
    <!-- <div>
      <router-link to="/">去首页 </router-link>
      <router-link to="/about">去关于</router-link>
    </div>   -->
    <div>
      <a class="go" @click="go('#/')">点击首页 &nbsp;&nbsp;</a>
      <a class="go"  @click="go('#/about')">点击关于</a>
    </div>
    <br>
    <router-view></router-view>
  </div>
</template>

<script>

let clipboardWrite = () => {
  alert('请yarn dev 在electron环境下操作')
};
if (window.electron) {
const { clipboard } = window.electron;
  clipboardWrite = function (text) {
    clipboard.writeText(text);
    alert('复制成功')
  };
}

export default {
  name: "App",
  components: {
  },
  data() {
    return {
      val: 'hello electron'
    };
  },
  methods: {
    copy() {
      clipboardWrite(this.val)
    },
    go (path) {
      location.href = path
    }
  },
};
</script>

<style lang="less" scoped>

</style>
