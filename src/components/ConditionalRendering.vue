<script setup>
import { computed, ref } from 'vue';

const isTrue = true;
const isFalse = false;

let isVisible = ref(true);

let isLoggedIn = ref(true);
let userName = 'Shayan';
let showDetails = computed(() => isLoggedIn.value);

const isActive = ref(true);

let password = ref('123456789');
</script>

<template>
    <dev>
        <p v-if="isTrue">This will show if isTrue is true.</p>
        <p v-else-if="isFalse">This will show if isFlase is true.</p>
        <p v-else>This will show if neither isTrue nor isFalse is true.</p>

        <p v-show="isVisible">This paragraph will be shown or hidden based on the value of isVisible.</p>
        <button @click="isVisible = !isVisible">Toggle Visibility</button>
    </dev>

    <dev>
        <h1 v-if="isLoggedIn">Welcome, {{ userName }}</h1>
        <p v-else>Please login to access this content.</p>

        <div v-show="showDetails">
            <h4>You're now abel to modify your Dashboard.</h4>
        </div>

        <button @click="isLoggedIn = !isLoggedIn">{{ isLoggedIn ? 'Logout' : 'Login' }}</button>
    </dev>
    <br>
    <dev v-if="isActive">
        <h1>My Blog Post</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt harum atque vitae ratione? Iste culpa, nam
            doloribus eius libero mollitia laudantium reprehenderit provident non voluptate ad asperiores pariatur fugit
            cupiditate.
        </p>
    </dev>
    <button @click="isActive = !isActive">Toggle</button>

    <div>
        <h1 v-if="password.length > 8">Strong Password</h1>
        <h1 v-else-if="password.length < 8">Weak Password</h1>
        <h1 v-else>Please enter your password</h1>
    </div>
</template>