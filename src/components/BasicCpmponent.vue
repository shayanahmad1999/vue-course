<script setup>
import { ref, watch } from 'vue';

const message = ref('Hello, Vue!');
const inputText = ref('');

watch(inputText, (newValue, oldValue) => {
    console.log(oldValue);
    message.value = `You typed: ${newValue}`;
});

</script>
<template>
    <h1>Work on Watches</h1>
    <h2>{{ message }}</h2>
    <input v-model="inputText" placeholder="Type something..." />
</template>