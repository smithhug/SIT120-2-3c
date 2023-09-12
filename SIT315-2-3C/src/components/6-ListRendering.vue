<script setup>
    import { reactive, ref } from 'vue';
    import sampleComponent from './sampleComponent.vue';

    const bgobject = reactive({
        title: 'Baldurs Gate III',
        score: 90
    })

    const awesomegames = ref([
        {
            title: 'Baldurs Gate III',
            score: 90
        },
        {
            title: 'Metal Gear Solid 2: Sons of Liberty',
            score: 100
        },
        {
            title: 'Shenmue',
            score: 60
        }
    ])
</script>

<template>
    <h1>6. List Rendering</h1>

    <h3>a- v-for with Object</h3> <!--a- v-for with Object-->
    <li v-for="(value, key) in bgobject">
        {{ key }}: {{ value }}
    </li>

    <br>

    <h3>b- v-for with Range</h3> <!--b- v-for with Range-->
    <li v-for="n in 4">{{n}}</li>

    <br>

    <h3>c- v-for with &lt;template></h3> <!--b- v-for with Range-->
    <ul>
        <template v-for="game in awesomegames">
            <li>Title: {{ game.title }} - Score: {{ game.score }}</li>
        </template>
    </ul>

    <h3>d- v-for with v-if</h3> <!--d- v-for with v-if -->
    <p>games with a score of 80+</p>
    <template v-for="game in awesomegames">
        <li v-if="game.score > 80">
            {{ game.title }}
        </li>
    </template>

    <h3>e- v-for with Component</h3> <!--e- v-for with Component-->
    <sampleComponent v-for="game in awesomegames" :title="game.title"/>
</template>