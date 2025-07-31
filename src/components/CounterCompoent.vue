<script setup>
import { useCounter } from '@/shared/useCounter';

const counter = useCounter();
</script>

<template>
    <h1>Composable</h1>
    <p>--the function or set of function in which we reuse the logic in overall application</p>
    <h3>Count: {{ counter.count }}</h3>
    <button @click="counter.increment">+</button>
    <button @click="counter.decrement">-</button>
</template>