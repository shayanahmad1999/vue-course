<script setup>
const google = "https://www.google.com/";
const amazingImage = "https://fastly.picsum.photos/id/0/5000/3333.jpg?hmac=_j6ghY5fCfSD6tvtcV74zXivkJSPIfR9B8w34XeQmvU";
const imageWidth = 500;
const imageHeight = 300;
const altText = "just a random picture";

// dynamic binding
const imageInfo = {
    src: "https://fastly.picsum.photos/id/20/3670/2462.jpg?hmac=CmQ0ln-k5ZqkdtLvVO23LjVAEabZQx2wOaT4pyeG10I",
    alt: 'just a random image',
    width: 700,
    height: 300
};
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

    <!-- dynamic binding -->
    <p>Dynamic Bindings</p>
    <img v-bind:="imageInfo" />
</template>