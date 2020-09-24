<template>
  <div id="app">
    <button @click="copy">复制下面这段字</button>
    <input type="text" v-model="val">
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
  },
};
</script>

<style lang="less" scoped>

</style>
