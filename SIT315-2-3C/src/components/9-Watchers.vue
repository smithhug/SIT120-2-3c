<script setup>
import { ref, watch } from 'vue';

const counter = ref(0);

//watch the counter value and report when it changes
watch(counter, (newValue, oldValue) => {
    alert(`Counter changed from ${oldValue} to ${newValue}`);
});

const incrementCounter = () => {
    counter.value++;
};

</script>

<template>
    <h1>9. Watchers</h1>
    <p>Counter: {{ counter }}</p>
    <button @click="incrementCounter">Increment</button>
</template>
