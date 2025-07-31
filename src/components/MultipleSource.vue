<script setup>
import { ref, watch } from 'vue';

const count = ref(0);
const userName = ref('Jordon');

watch([count, userName], (newValue, oldValue) => {
    console.log('new value', newValue);
    console.log('old value', oldValue);
})
</script>
<template>
    <h2>Name: {{ userName }}</h2>
    <h2>Count: {{ count }}</h2>

    <button @click="userName = 'Jhon'">Change Name</button>
    <button @click="count++">Count</button>
</template>