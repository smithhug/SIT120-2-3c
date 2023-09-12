<template>
    <h1>5. Class and Style Bindings</h1>
    <p v-bind:class="{'redtext' : true}">This text is bound by class and will therefore be red!</p>
    <p v-bind:style="{'color': 'blue'}">This text is bound by inline style and will therefore be blue!</p>
</template>

<style scoped>
.redtext {
    color: red;
}
</style>