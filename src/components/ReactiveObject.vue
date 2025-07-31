<script setup>
import { reactive, watch } from 'vue';

let state = reactive({ username: 'Jhon' });

watch(() => state.username, (newValue, oldValue) => {
    console.log('new value', newValue);
    console.log('old value', oldValue);
});
</script>
<template>
    <h2>{{ state.username }}</h2>
    <button @click="state.username = 'Jordon'">change name</button>
</template>