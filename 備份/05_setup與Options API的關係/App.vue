<template>
    <!-- html -->
    <Person/>
</template>

<script lang="ts">
    //  JS或TS
    import Person from './components/Preson.vue'

    export default{
        name: 'App', //組件名
        components: {Person}
    }
</script>
