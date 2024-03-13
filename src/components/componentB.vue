<script setup>
import {ref} from 'vue'
const test = ref('test')
// const dataList={
//     key1:'a',
//     key2:'b',
//     key3:'c',
//     key4:'d'
// }
setTimeout(()=>{
    test.value='apple!'
},2000)
</script>
<template>
    <p class="test-cls":key="test">{{ test }}</p>
    <!-- <p v-for="(value,key,index) in dataList"
    :key="value"
    >
        <span v-show="key!=='key3'">
            {{index}},{{ key }},{{ value }}
        </span>
   
    </p> -->
</template>
<style scoped>
.test-cls{
    font-size: 40px;
    animation: openIn 1s ease-in-out;
}
@keyframes openIn{
    0%{
        opacity: 0;
        transform: translateY(20px);
    }
    100%{
        opacity: 1;
        transform: translateY(0);
    }
}
</style>