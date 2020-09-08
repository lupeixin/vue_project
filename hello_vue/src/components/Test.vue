<!--组件的template  内部只能有一个根标签-->
<template>
    <!--  不同有同级的标签  -->
    <div>
       这是我的第一个组件====组价使用成功
        <br>
        <span>这是一节多么快乐而又优秀的课程啊！！！</span>
    </div>

</template>

<!--编写js代码的地方  当前对象就是组件对象-->
<script>
    export default {
        name: "Test"
    }
</script>

<!--用来为当前组件指定样式  scoped: 脚手架提供的属性  加上此属性代表当前样式只在当前组件生效 -->
<style scoped>
    div {
        color: green;
    }
    span {
        color: darkmagenta;
    }

</style>
