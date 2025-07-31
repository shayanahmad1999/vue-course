<script setup>
let myRefFunc = (el) => {
    console.log(el.textContent);
    el.textContent = "Text changed";
    el.style.color = "crimson";
}
</script>
<template>
    <h3 :ref="myRefFunc">This is inital value</h3>
</template>