<script setup>
const props = defineProps(['name']);
</script>

<template>
    <h1>Props (Static Props)</h1>
    <h2>Props (Short of Properties) pass data from parent to child component.</h2>
    <h3>{{ props.name }}</h3>
</template>