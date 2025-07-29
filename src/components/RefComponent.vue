<script setup>
import { reactive, ref } from 'vue';

const count = ref(0);

let userName = ref('');

let userList = ref(['shayan', 'hanif', 'asad']);

let userInfo = ref({ name: 'shayan', age: 25, location: ['peshawar', 'kpk'], isMaried: false });

let friends = reactive([ref('shayan'), ref('hanif'), ref('asad'), ref('hilal')]);
</script>
<template>
    <h1>Ref</h1>
    <h2>Simple Example</h2>
    <h3>Count: {{ count }}</h3>
    <button @click="count++">+</button>
    <button @click="count--">-</button>

    <h2>Complex Example (A)</h2>
    <h3>User Name: {{ userName }}</h3>
    <button @click="userName = 'Shayan'">Add User</button>

    <h2>Complex Example (B)</h2>
    <h3>User Lists: {{ userList }}</h3>
    <button @click="userList.push('Hilal')">Add User</button>

    <h2>Complex Example (C)</h2>
    <h3>User Information: {{ userInfo }}</h3>
    <h4>User Name: {{ userInfo.name }}</h4>
    <h4>User Age: {{ userInfo.age }}</h4>
    <h4>User Location: {{ userInfo.location }}</h4>
    <h4>User Status: {{ userInfo.isMaried }}</h4>
    <button @click="userInfo.name = 'John Doe'">Change Name</button>
    <button @click="userInfo.age = 40">Change Age</button>
    <button @click="userInfo.location = ['New York', 'USA']">Change Location</button>
    <button @click="userInfo.isMaried = true">Change Status</button>

    <h2>Complex Example (D)</h2>
    <h2>Array of Ref</h2>
    <h3>1. {{ friends[0] }}</h3>
    <h3>2. {{ friends[1] }}</h3>
    <h3>3. {{ friends[2] }}</h3>
    <h3>4. {{ friends[3] }}</h3>

    <button @click="friends[0] = '🤝'">Hand Shake</button>
    <button @click="friends[1] = '🫂'">Hug</button>
    <button @click="friends[2] = '😊'">Smile</button>
    <button @click="friends[3] = '😎'">Attitude</button>

</template>