<template>
     <div class="person">
        <h2>姓名: {{name}}</h2>
        <h2>年齡: {{age}}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年齡</button>
        <button @click="showNo">查看編號</button>
     </div>
</template>

<script lang="ts">
    export default {
        name: 'Person',
        data(vm) {
            return {
                name: '喵咪',
                age: 2,
                no: '123456789',
            }
        },
        methods:{
            changeName(){
                this.name = 'meow'
            },
            changeAge(){
                this.age += 1
            },
            showNo(){
                alert(this.no)
            }
        }
    }
</script>

<style>
    .person {
        background-color: lightpink;
        padding: 20px;
    }
    button {
        margin: 0 8px;
    }
</style>