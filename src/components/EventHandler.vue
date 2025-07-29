<script setup>
import { ref } from 'vue';

const count = ref(0);

const increment = () => count.value++;
const decrement = () => count.value--;

const formSubmit = (e) => {
    e.preventDefault();
    alert('valid credentials');
}

const showMessage = (message) => alert(message);

</script>

<template>
    <h1 class="default">Count: {{ count }}</h1>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>

    <form @submit="formSubmit">
        <input type="text" placeholder="Enter your name...">
        <input type="email" placeholder="Enter your email...">
        <button type="submit">Submit</button>
    </form>

    <button @click="showMessage('i am here')">Show Message</button>
</template>

<style scoped>
.default {
    color: black;
}
</style>