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
        setup() {
            // setup中的this是undefined，Vue3中已經弱化this了
            // data
            // 此時的變數不是響應式的
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


            // return {name, age, changeName, changeAge, showNo}

            // setup的return也可以是渲染函式
            // return function(){
            //     return '哈哈'
            // }

            // return ()=> {
            //     return '哈哈'
            // }

            // return ()=> '哈哈'
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