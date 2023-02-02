<script setup>
import Language from './language.vue';
import Counter from './Counter.vue';

defineProps({
  msg: {
    type: String,
    required: true
  }
})

function test() {
  alert('alert');
}

const items = [{color: 'red', text: 'javascript'}, {color: 'blue', text: 'html'}, {color: 'orange', text: 'css'}];
</script>

<template>
  <div class="greetings">
    <h1 class="green" @click="test">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>

    <ul>
      <Language v-for="item in items" :color="item.color">{{ item.text }}</Language>
    </ul>

    <Counter />
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
