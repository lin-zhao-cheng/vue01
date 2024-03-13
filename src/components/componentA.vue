<script setup>
import { ref, onMounted } from 'vue'
const data="Hi Vue 351454"
const text = ref("123")
</script>


<template>

<p> 單向綁定</p>
{{ data }}

<p> 雙向綁定</p>
<input type="text" v-model="text"/>
<p>{{ text }}</p>

</template>





<style scoped>

</style>