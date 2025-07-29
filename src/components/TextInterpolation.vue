<script setup>
const myMessage = 'Yellow World';
const myNumber = 10;
function add(x, y) {
    return x + y;
}
</script>

<template>
    <h1>Text Interpolation</h1>
    <p>Message: {{ myMessage }}</p>
    <p>Number: {{ myNumber }}</p>
    <p>Add Two Numbers: {{ add(2, 11) }}</p>
</template>