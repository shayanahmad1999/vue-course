<script setup>
import axios from 'axios';
import { ref } from 'vue';

const data = ref(null);
const fetchData = async () => {
    try {
        const response = await axios.get('https://jsonplaceholder.typicode.com/posts');

        data.value = response.data;
    } catch (error) {
        console.log(`Error fetching Data: ${error}`);
    }
}
</script>
<template>
    <h1>((Using axios))</h1>
    <button @click="fetchData">Fetch Data</button>
    <div>
        <h2>Data from API:</h2>
        <pre>{{ data }}</pre>
    </div>
</template>