<script setup></script>
<template>
    <h2>child used $emit (emit event)</h2>
    <button @click="$emit('incrementCounter')">+</button>
    <button @click="$emit('decrementCounter')">-</button>
</template>

<style scoped>
button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
</style>