<template>
     <div class="person">
        <h2>姓名: {{name}}</h2>
        <h2>年齡: {{age}}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年齡</button>
        <button @click="showNo">查看編號</button>
        <h2>data_a: {{a}}</h2>
     </div>
</template>

<script lang="ts">
    export default {
        name: 'Person',
        data(){
            return{
                a: this.name
            }
        },
        setup() {
            // data
            let name = '喵三';
            let age = 18;
            let no = '123456789';

            // methods
            function changeName(){
                name = 'meow';
                // name確實改了，但不是響應式變數，所以修改後頁面沒有變化
            }
            function changeAge(){
                age += 1
            }
            function showNo(){
                alert(no)
            }

            return {name, age, changeName, changeAge, showNo}
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