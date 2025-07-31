<script setup>
import { onMounted, ref } from 'vue';
import TemplateRefComponent2 from './TemplateRefComponent2.vue';

const myRef = ref(null);

onMounted(() => {
    console.log(myRef.value);
});

</script>

<template>
    <TemplateRefComponent2 ref="myRef" />
</template>