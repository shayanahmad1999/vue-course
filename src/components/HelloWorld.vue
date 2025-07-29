<!-- JS -->
<script setup>
import NestedComponent from './NestedComponent.vue';

console.log('Hello World from console');
</script>

<!-- HTML -->
<template>
    <h1>Hello World</h1>
    <h2>This is Parent Component</h2>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, maiores facere quis exercitationem at libero,
        labore
        provident dolores eius, quam natus earum quo. Voluptates error et consectetur cupiditate perspiciatis veritatis?
    </p>
    <NestedComponent />
</template>

<!-- CSS -->
<style>
h1 {
    color: rgb(16, 130, 92);
}
</style>