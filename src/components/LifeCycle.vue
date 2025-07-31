<script setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated, ref } from 'vue';

let message = ref('Hello, Vue!');

let updateMessage = () => {
    message.value = "Hello, Vue js!";
};

onBeforeMount(() => {
    console.log('Component is about to be mounted');
});

onMounted(() => {
    console.log('Component has been mounted');
});

onBeforeUpdate(() => {
    console.log('Component is about to be update');
});

onUpdated(() => {
    console.log('Component has been update');
});

onBeforeUnmount(() => {
    console.log('Component is about to be unmounted');
});

onUnmounted(() => {
    console.log('Component has been unmounted');
})

</script>
<template>
    <h1>LifeCycle Hook</h1>
    <h2>{{ message }}</h2>
    <button @click="updateMessage">Update Message</button>
</template>