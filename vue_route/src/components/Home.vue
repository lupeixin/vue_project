<template>
    <div>
        <h3>留言板</h3>
        <input type="text" v-model="msg">
        <button @click="add_note">发表留言</button>
        <br>
        <ul>
            <li v-for="(m, index) in msg_list">{{m}} | <button @click="remove(index)">删除</button></li>
        </ul>
        <hr>
        <span>留言数：{{msg_list.length}}</span> &nbsp;&nbsp;&nbsp;&nbsp; <button @click="clear">清空留言</button>

    </div>
</template>

<script>
export default {
    name: "Home",
    data: function (){
        return {
            msg: '',
            msg_list: localStorage.msgs ? JSON.parse(localStorage.msgs) :[],
        }
    },
    methods: {
        add_note(){
            let msg = this.msg;
            if (msg){
                this.msg_list.push(this.msg);
                localStorage.msgs = JSON.stringify(this.msg_list);
                this.msg = '';
            }
        },
        remove(index){
            let val = JSON.parse(localStorage.msgs);
            val.splice(index,1);
            localStorage.msgs = JSON.stringify(val);
            this.msg_list = localStorage.msgs ? JSON.parse(localStorage.msgs) :[];
        },
        clear(){
            localStorage.clear();
            this.msg_list = localStorage.msgs ? JSON.parse(localStorage.msgs) :[];
        },

    }
}
</script>

<style scoped>

</style>
