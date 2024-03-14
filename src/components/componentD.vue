<script >
import {ref, createApp } from 'vue';

const vm = createApp({
setup(){
    const message = ref('Hello vue 3.0');
    return{
        message
    }
}
});
vm.mount('#app');
</script>
<template>
<div id="app">
  {{ message }}
</div>
</template>
<style scoped></style>