<script setup>
import {computed,ref} from 'vue'
const num = ref(0)

const numFormat = computed(()=>{
    console.log('change')
    if(Number.isNaN(num.value*100))return num
    return `${num.value*100}%`
})
//原生function寫法
// const numFormat=()=>{
//     if(Number.isNaN(num*100))return num
//     return `${num*100}%`
// }
</script>

<template>
<h1>Computed 計算屬性</h1>
<input type="number" v-model="num">

<h3>{{ numFormat }}</h3>
</template>

<style scoped></style>