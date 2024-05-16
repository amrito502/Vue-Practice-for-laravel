<script setup>
import {ref} from 'vue'
import useNumbers from './number'
let number = ref(0)

const {increment, decrement} = useNumbers(number)

</script>

<template>
   {{ number }}
   <button @click="increment">Increment</button>
   <button @click="decrement">Decrement</button>

   <!-- <button @click="number++">+</button>
   <button @click="number--">-</button>
</template> -->

<style scoped>

</style>
