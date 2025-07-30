<script setup>
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const password = ref('');

</script>
<template>
    <form @submit.prevent="$emit('userinfo', name, email, password)">
        <input type="text" placeholder="Enter your name..." v-model="name">
        <input type="email" placeholder="Enter your email..." v-model="email">
        <input type="password" placeholder="Enter your password..." v-model="password">
        <button type="submit">Submit</button>
    </form>
</template>