<script setup>
const props = defineProps({
    fullName: {
        type: String,
        required: true,
        default: 'Anonymous'
    },
    age: Number
});

</script>
<template>
    <h1>{{ props.fullName }}</h1>
    <h1>{{ props.age }}</h1>
</template>