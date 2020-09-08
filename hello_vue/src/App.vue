<template>
  <div id="app">

    <Test></Test>
    <Second></Second>

  </div>
</template>

<script>

// 注册组件时需要先将定义好的组件导入过来
import Test from "./components/Test"
import Second from "./components/Second";

export default {
  name: 'App',
  // 将导入的组件注册到根组件中
  components: {
    "Test": Test,
    Second: Second,
  }
}
</script>

<style>
</style>
