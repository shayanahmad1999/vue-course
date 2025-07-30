<script setup>
const props = defineProps(['first', 'last']);

//props are "immutable" which means there value cannot be changed
// --and they're just readonly.

// props.first = 'hanif'; // ❌❌❌
</script>

<template>
    <h1>Props (Dynamic Props)</h1>
    <h2>{{ first + ' ' + last }}</h2>
</template>