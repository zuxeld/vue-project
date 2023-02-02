<template>
    <p>{{ counter }}</p>
    <button @click="counter++">+</button>
    <button @click="counter--">-</button>
</template>


<script setup>
import { ref } from 'vue'

let counter = ref(0);


</script>