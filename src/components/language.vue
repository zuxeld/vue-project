<template>
    <li @click="test" :style="`background: ${color}`"><slot></slot></li>
</template>

<style scoped>
li {
    padding: 20px;
}
</style> 

<script setup>
import { useSlots } from 'vue'
const props = defineProps({
    color: String
})

const slots = useSlots()

function test(e) {
    console.log(slots.default()[0].children)
}
</script>