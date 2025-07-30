<script setup>
import { ref } from 'vue';
import EventsChild from './EventsChild.vue';
import EventsForm from './EventsForm.vue';

let count = ref(0)

let handleDecrement = () => {
    count.value--;
}

const formHandler = (name, email, password) => {
    console.log('Name', name);
    console.log('Email', email);
    console.log('password', password);
}
</script>
<template>
    <h2>parent used v-on or @ (listen event)</h2>
    <h1>Count: {{ count }}</h1>

    <EventsChild @incrementCounter="count++" @decrementCounter="handleDecrement" />

    <hr />

    <EventsForm @userinfo="formHandler" />

</template>