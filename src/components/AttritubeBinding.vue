<script setup>
const google = "https://www.google.com/";
const amazingImage = "https://fastly.picsum.photos/id/0/5000/3333.jpg?hmac=_j6ghY5fCfSD6tvtcV74zXivkJSPIfR9B8w34XeQmvU";
const imageWidth = 500;
const imageHeight = 300;
const altText = "just a random picture";
</script>

<template>
    <p>old binding</p>
    <!-- old binding -->
    <a v-bind:href="google">Google</a>

    <p>new binding</p>
    <!-- new binding -->
    <a :href="google">Google</a>

    <p>Amazing Image</p>
    <img :src="amazingImage" :width="imageWidth" :height="imageHeight" :alt="altText" />
</template>