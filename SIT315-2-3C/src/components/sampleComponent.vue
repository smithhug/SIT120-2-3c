<script setup>
    defineProps(['title'])
</script>

<template>
  <h5>
    - {{ title }}
  </h5>
</template>

<style scoped>
    h5 {
        color: cyan;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }
</style>