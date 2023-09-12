<script setup>
    import { reactive, computed } from 'vue';

    const number = 483;
    //This is where the computed properties occur
    const isNumberHigherThan45 = computed(() => {
        return number > 45 ? 'Yes' : 'No'
    })
</script>


<template>
    <h1>4. Computed Properties</h1>
    <p>Is the number {{ number }} higher than 45?</p>
    <span>{{ isNumberHigherThan45 }}</span>
</template>