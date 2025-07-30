<script setup>
import { ref } from 'vue';

let formData = ref({ name: '', email: '', password: '' });

let formSubmit = () => alert('form submitted');
</script>

<template>
    <div>
        <form @submit.prevent="formSubmit">
            <input type="text" v-model="formData.name" placeholder="Enter your name...">
            <input type="email" v-model="formData.email" placeholder="Enter your email...">
            <input type="password" v-model="formData.password" placeholder="Enter your password...">
            <button type="submit">Submit</button>
        </form>

        <h3>Enter Name: {{ formData.name }}</h3>
        <h3>Enter Email: {{ formData.email }}</h3>
        <h3>Enter Password: {{ formData.password }}</h3>
    </div>
</template>