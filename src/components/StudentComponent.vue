<script setup>
import { inject } from 'vue';

// defineProps(['name', 'age', 'location']);

const name = inject('name');
const age = inject('age');
const location = inject('location');
</script>
<template>
    <ul>
        <li>{{ name }}</li>
        <li>{{ age }}</li>
        <li>{{ location }}</li>
    </ul>
</template>