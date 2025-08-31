<template>
     <div class="person">
        <h2>姓名: {{name}}</h2>
        <h2>年齡: {{age}}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年齡</button>
        <button @click="showNo">查看編號</button>
     </div>
</template>

<script lang="ts" setup name="Person">
    import {ref} from 'vue'

    // data
    let name = ref('喵三');
    let age = ref(18);
    let no = '123456789';

    // console.log(name);
    // console.log(age);

    // methods
    function changeName(){
        name.value = 'meow';
    }
    function changeAge(){
        age.value += 1
    }
    function showNo(){
        alert(no)
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