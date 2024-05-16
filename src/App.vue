<script setup>
import {ref} from 'vue'

let number = ref(0)

setInterval(() => {

 number.value++
}, 1000)


</script>

<template>
 {{ number }}
</template>

<style scoped>

</style>
