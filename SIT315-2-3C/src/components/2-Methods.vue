<script>
export default {
    data() {
        return {
            counter: 0
        };
    },
    methods: { //here are the two methods
        incrementCounter() {
            this.counter++;
        },
        decreaseCounter() {
            this.counter--;
        }
    }
};
</script>

<template>
    <h1>2. Methods</h1>
    <p>Counter: {{ counter }}</p>
    <button @click="incrementCounter">Increment</button>
    <button @click="decreaseCounter">Decrease</button>
</template>