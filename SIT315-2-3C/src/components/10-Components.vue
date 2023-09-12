<script setup>
    defineProps(['title'])
    defineEmits(['enlarge-text'], 
                ['reduce-text'])
</script>

<template>
    <h1>10. Components</h1>

    <p> The 'title' prop passed through was: {{ title }}</p> <!--a - Props-->

    <button @click="$emit('enlarge-text')">Enlarge</button> <!--b - Events using $emit -->
    <button @click="$emit('reduce-text')">Reduce</button>

    <br>
    <slot></slot> 
    <!--c - Slots -->

</template>