<script setup>
    import { ref } from 'vue';

    const inlinecount = ref(0)

    function soundalarm() {
        alert('Warning!: Stop pushing buttons!')
    }
</script>

<template>
    <h1>7. Event Handling</h1>

    <p>The inline count is: {{ inlinecount }}</p> <!--a- Inline Handling-->
    <button @click="inlinecount++">Increment</button>

    <p>Press below to see a method in action</p>
    <button @click="soundalarm">Sound the alarm</button> <!--b- Method Handling-->
</template>