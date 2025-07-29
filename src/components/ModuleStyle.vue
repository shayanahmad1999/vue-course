<template>
    <h1 :class="$style['kabab-case']">Using Module CSS with $ syntax (kabab-case)</h1>
    <h1 :class="$style['camalCase']">Using Module CSS with $ syntax (camalCase)</h1>
</template>

<style module>
.kabab-case {
    background-color: fuchsia;
    color: white;
}

.camalCase {
    background-color: seagreen;
    color: white;
}
</style>