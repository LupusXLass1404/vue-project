<template>
    <!-- html -->
     <div class="app">
        <h1>你哈</h1>
        <Person/>
     </div>
</template>

<script lang="ts">
    //  JS或TS
    import Person from './components/Preson.vue'

    export default{
        name: 'App', //組件名
        components: {Person}
    }
</script>

<style>
    /* 樣式 */
    .app {
        background-color: skyblue;
        padding: 20px;
    }
</style>