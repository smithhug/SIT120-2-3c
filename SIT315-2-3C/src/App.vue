<script setup>
import { ref, computed } from 'vue';

import TemplateSyntax from './components/1-TemplateSyntax.vue';
import Methods from './components/2-Methods.vue';
import ReactivityFundamentals from './components/3-ReactivityFundamentals.vue';
import ComputedProperties from './components/4-ComputedProperties.vue';
import ClassAndStyleBindings from './components/5-ClassAndStyleBindings.vue';
import ListRendering from './components/6-ListRendering.vue';
import EventHandling from './components/7-EventHandling.vue';
import FormInputBindings from './components/8-FormInputBindings.vue';
import Watchers from './components/9-Watchers.vue';
import Components from './components/10-Components.vue';

const allFontSize = ref(1);

const routes = {
  '/template-syntax': TemplateSyntax,
  '/methods': Methods,
  '/reactivity-fundamentals': ReactivityFundamentals,
  '/computed-properties': ComputedProperties,
  '/class-and-style-bindings': ClassAndStyleBindings,
  '/list-rendering': ListRendering,
  '/event-handling': EventHandling,
  '/form-input-bindings': FormInputBindings,
  '/watchers': Watchers,
  '/components': Components,
};

const currentPath = ref(window.location.hash);

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash;
});

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'];
});

</script>

<template>
  <div :style="{ fontSize: allFontSize + 'em' }">
    <p> 11. Routes </p>
    <div>
      <a href="#/template-syntax">Template Syntax</a>
      <a href="#/methods">Methods</a>
      <a href="#/reactivity-fundamentals">Reactivity Fundamentals</a>
      <a href="#/computed-properties">Computed Properties</a>
      <a href="#/class-and-style-bindings">Class and Style Bindings</a>
      <a href="#/list-rendering">List Rendering</a>
      <a href="#/event-handling">Event Handling</a>
      <a href="#/form-input-bindings">Form Input Bindings</a>
      <a href="#/watchers">Watchers</a>
      <a href="#/components">Components</a>
    </div>
    <!-- Render the current component based on the route -->
    <component :is="currentView"
      title="This is a props example"
      @enlarge-text="allFontSize += 0.1"
      @reduce-text="allFontSize -= 0.1"
      >This is the slotted body</component>


  </div>
</template>

<style scoped>
  a {
    display: inline-block;
    margin-right: 2px;
    background-color: gray;
    padding: 5px;
    color: white;
  }
</style>