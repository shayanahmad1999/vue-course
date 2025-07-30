<script setup>
defineProps({
    friends: Array,
    userInfo: Object
});
</script>

<template>
    <h3>{{ friends }}</h3>
    <h3>{{ userInfo }}</h3>

    <!-- Iterating Over Friends Array -->
    <ul v-for="(friend, index) in friends" :key="index">
        <li>{{ friend }}</li>
    </ul>

    <hr />

    <ul v-for="(info, i) in userInfo" :key="i">
        <li>{{ info }}</li>
    </ul>
</template>