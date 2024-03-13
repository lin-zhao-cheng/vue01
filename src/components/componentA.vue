<script setup>
import { ref, onMounted } from 'vue'
const data="Hi Vue 351454"
const text = ref("123")
const view = ref(1)
const changeView=(index)=>{
    view.value = index
}
// const changeView2=()=>{
//     view.value = 1
// }
</script>


<template>
    <button v-on:click="changeView(1)">顯示單向綁定</button>
    <button @click="changeView(2)">顯示雙向綁定</button>
    <button @click="changeView(333)">沒畫面</button>
<div class="container01" v-if="view===1">
    <p> 資料單向綁定</p>
    {{ data }}
</div>

<div class="container02" v-if="view===2">
    <p> 資料雙向綁定</p>
    <input type="text" v-model="text"/>
    <p>{{ text }}</p>
</div>
<div v-else>沒畫面</div>

</template>





<style scoped>
.container01{
    border: 2px red solid;
}
.container02{
    border: 2px blue solid;
}
</style>