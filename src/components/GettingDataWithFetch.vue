<script setup>
import { ref } from 'vue';

const data = ref(null);

const fetchData = () => {
    fetch('https://jsonplaceholder.typicode.com/posts')
        .then((response) => {
            if (!response) {
                throw new Error(`HTTP Error! Status: ${response.status}`);
            }
            return response.json();
        })
        .then((responseData) => {
            data.value = responseData;
        })
        .catch((error) => {
            console.log(`Error fetching data: ${error}`);
        });
}
</script>

<template>
    <h1>((Using fetch))</h1>
    <button @click="fetchData">Fetch Data</button>
    <div>
        <h2>Data from API:</h2>
        <pre>{{ data }}</pre>
    </div>
</template>