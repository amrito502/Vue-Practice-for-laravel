<script setup>
import { ref, computed } from "vue"

const zip = ref("")

const zipUppercase = computed({
 get: () => zip.value.toUpperCase(),
 set: value => { zip.value = value.toUpperCase() }
})

</script>

<template>
  <div>
    <input type="text" v-model="zipUppercase">
    {{ zip }}
  </div>
</template>

<style scoped>
</style>
