<script>
export default {
  data() {
    return {
      msg: 'This is a demonstration of Text Interpolation',
      rawHtml: 'This is an example of Raw HTML',
      link: 'https://www.google.com'
    };
  }
};
</script>

<template>
    <h1>1. Template Syntax</h1>
    <span>Message: {{ msg }}</span> <!--a) Text Interpolation-->

    <p>Using v-html directive: <span v-html="rawHtml"></span></p> <!--b) Raw HTML -->

    <a v-bind:href="link">Visit Google</a> <!--c) Atribute binding (link bind)-->
    <br><br>

    {{ number = 1 + 4 }} <!--d) Javascript expression-->

    <p>"The number is: {{ number }}"</p> 

</template>