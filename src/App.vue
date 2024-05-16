<script setup>
import {ref, reactive} from 'vue'

const form = reactive({
  name: "Amrito",
  password: "password"
})

// let name = ref("Amrito")

// setInterval(() => {
// name.value = "Sakib"
// }, 1000)


</script>

<template>
 {{ form.name }} {{ form.password }}
  <!-- {{ name }} -->
</template>

<style scoped>

</style>
