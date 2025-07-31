<script setup>
import { onMounted, ref } from 'vue';

const myRef = ref('');

onMounted(() => {
    console.log(myRef.value);
    myRef.value.focus()
    myRef.value.value = 'somthing...'
});
</script>
<template>
    <h1>Template Ref</h1>
    <div>
        <input type="text" placeholder="Enter your name" ref="myRef">
    </div>
</template>