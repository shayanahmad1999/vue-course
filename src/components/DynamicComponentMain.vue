<script setup>
import { ref } from 'vue'
import ComponentOne from './DynamicComponentOne.vue'
import ComponentTwo from './DynamicComponentTwo.vue'
import ComponentThree from './DynamicComponentThree.vue'

const currentTab = ref('ComponentOne')

const tabs = {
    ComponentOne: ComponentOne,
    ComponentTwo: ComponentTwo,
    ComponentThree: ComponentThree
}
</script>

<template>
    <!-- With Dynamic Component -->
    <button @click="currentTab = 'ComponentOne'">What is HTML</button>
    <button @click="currentTab = 'ComponentTwo'">What is CSS</button>
    <button @click="currentTab = 'ComponentThree'">What is JS</button>

    <component :is="tabs[currentTab]" />
</template>