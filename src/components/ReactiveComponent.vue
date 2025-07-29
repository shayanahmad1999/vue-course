<script setup>
import { reactive } from 'vue';

const initailState = reactive({ count: 0 });

const complexInitialState = reactive({ val: { count: 0 }, user: ['shayan', 'hanif'] });

const changeUser = () => {
    complexInitialState.user[0] = 'Asad'
    complexInitialState.user[1] = 'Hilal'
}
</script>

<template>
    <h1>Reactivity & Reactive</h1>
    <h2>Simple Example</h2>
    <h3>Count: {{ initailState.count }}</h3>
    <button @click="initailState.count++">+</button>
    <button @click="initailState.count--">-</button>

    <h2>Complex Example</h2>
    <h3>Current Count: {{ complexInitialState.val.count }}</h3>
    <h3>Users: {{ complexInitialState.user }}</h3>

    <button @click="complexInitialState.val.count += 10">Add 10</button>
    <button @click="changeUser">Change User</button>
    <button @click="complexInitialState.user.push('John Doe')">Add User</button>
</template>