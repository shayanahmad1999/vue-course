<script setup>
import { ref } from 'vue';

const count = ref(0);
const increment = () => count.value++;
const decrement = () => count.value--;

defineExpose({ count, increment, decrement });
</script>

<template>
    <h3>Count: {{ count }}</h3>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
</template>