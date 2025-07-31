<script setup>
import { ref, defineAsyncComponent } from 'vue';

const RenderFriends = defineAsyncComponent(() => import('./RenderFriends.vue'));

const showHide = ref(false);

const toggleFriends = () => {
    showHide.value = !showHide.value;
}
</script>
<template>
    <div v-if="showHide">
        <RenderFriends />
    </div>
    <button @click="toggleFriends">show / hide</button>
</template>