<template>
    <div>
        这是我的用户组件

        <h3>用户列表页</h3>
        <table border="1" cellspacing="0">
            <tr>
                <td>ID</td>
                <td>姓名</td>
                <td>生日</td>
                <td>个人信息</td>
                <td>操作</td>
            </tr>
            <tr v-for="(user, index) in users" :key="index">
                <td>{{user.id}}</td>
                <td>{{user.username}}</td>
                <td>{{user.bir}}</td>
                <td>{{user.content}}</td>
                <td><button @click="del(index)">删除</button> | <router-link :to="`/detail/${user.id}`">查看用户详情</router-link>
                </td>
            </tr>
        </table>


    </div>
</template>

<script>
export default {
    name: "User",
    data: function () {
        return {
            users: [
                {id: 1, username: "小黑", bir: "2012-12-12", content: "自我介绍"},
                {id: 2, username: "小白", bir: "2013-12-12", content: "自我介绍"},
                {id: 3, username: "小红", bir: "2014-12-12", content: "自我介绍"},
            ]
        }
    },
    methods: {
        goDetail(user_id){
            // 跳转到详情页  并且传递id过去
        },
        del(index){
            let users = this.users;
            this.users.splice(index, 1);
            this.users = users;
        }
    }
}
</script>

<style scoped>

</style>
