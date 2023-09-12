<script>
    import { ref } from 'vue';

    const msg = ref('')
    const check = ref(false)
    const radioval = ref('Small')
    const selected = ref('')

    export default {
        data() {
            return {
                msg: '',
                check: false,
                radioval: 'Small',
                selected: '',
                lazymessage: '',
                numberage: 0,
                username: ''
            };
        }
    };


</script>

<template>
    <h1>8. Form Input Bindings</h1>

    <p>Text demo: {{ msg }}</p> <!--Text input-->
    <input v-model="msg"/>

    <p>Box status: {{ check }}</p> <!--Checkbox input-->
    <input type="checkbox" v-model="check" />

    <p>Radio selected: {{ radioval }}</p> <!--Radio Input-->
    <input type="radio" id="small" value="Small" v-model="radioval"/>
    <label for="small">Small</label>
    <input type="radio" id="large" value="Large" v-model="radioval"/>
    <label for="large">Large</label>

    <p>Selected meal: {{ selected }}</p> <!--Select Input-->
    <select v-model="selected">
        <option disabled value="">Please select a meal</option>
        <option>Pasta</option>
        <option>Steak</option>
        <option>Chicken</option>
    </select>

    <br>

    <p>Lazy message: {{ lazymessage }}</p> <!--.lazy-->
    <input v-model.lazy="lazymessage" type="text" placeholder="Enter your message">

    <p>Age: {{ numberage }}</p> <!--.number-->
    <input v-model.number="numberage" type="number" placeholder="Enter your age">

    <p>Your Username: {{ username }}</p> <!--.trim-->
    <input v-model.trim="username" type="text" placeholder="Enter your username">


</template>