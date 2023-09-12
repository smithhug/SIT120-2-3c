<script setup>
    import { ref } from 'vue';

    // We will do the increment button again using ref
    const count = ref(0);

    function increment() {
      count.value++;
    }

</script>

<template>
    <h1>3. Reactivity Fundamentals</h1>
    <button @click="increment">
        {{ count }}
    </button>
</template>