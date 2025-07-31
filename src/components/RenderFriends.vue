<script setup>
import { ref } from 'vue';

const friends = ref(['shayan', 'hanif', 'asad', 'hilal']);
</script>
<template>
    <h3 v-for="(frnd, i) in friends" :key="i">
        {{ frnd }}
    </h3>
</template>