<script setup>
import { computed, ref } from 'vue';

const number = ref(5);

const squaredNumber = computed(() => {
    return number.value * number.value;
});

const firstName = ref('Shayan');
const lastName = ref('Ahmad');

const fullName = computed(() => firstName.value + ' ' + lastName.value);

const counter = ref(0);

const squaredCounter = computed(() => counter.value ** 2);

const incrementCounter = () => {
    counter.value++;
}
</script>
<template>
    <h1>Computed Properties</h1>
    <h2>Original Number: {{ number }}</h2>
    <h2>Squared Number: {{ squaredNumber }}</h2>

    <h2>First Name: {{ firstName }}</h2>
    <h2>Last Name: {{ lastName }}</h2>
    <h2>Full Name: {{ fullName }}</h2>

    <h2>Counter: {{ counter }}</h2>
    <h2>Squared Counter: {{ squaredCounter }}</h2>
    <button @click="incrementCounter">Increment Counter</button>
</template>