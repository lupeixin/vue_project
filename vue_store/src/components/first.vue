<template>
  <div>第一个组件
    <el-button @click="add">按钮</el-button>
  </div>
</template>

<script>
export default {
  name: "first",
  methods:{
    add(){
      this.$store.commit("add_count")
    },
  }
}
</script>

<style scoped>

</style>
