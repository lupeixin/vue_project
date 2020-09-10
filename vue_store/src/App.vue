<template>
  <div id="app">

    <first></first>
    <hr>
    <second></second>
    <router-view></router-view>
  </div>
</template>

<script>
import first from "./components/first";
import second from "./components/second";

export default {
  name: "App",
  components: {
    first: first,
    second:second,
  }
}
</script>

<style>

</style>
