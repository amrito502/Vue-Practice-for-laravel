<script setup>
let msg = "Welcome Amrito!"
let dynamicId = 2
let isButtonDisabled = true
const objectOfAttrs = {
  id: "container",
  class: "wrapper"
}
let seen = false
let google = "https://google.com"
const clickMe = () => {
  console.log('Click')
}
</script>

<template>
  {{ msg }}
  <div v-html="msg"></div>

  <div v-bind:id="dynamicId">dynamicid</div>
  <button :disabled="isButtonDisabled">button</button>
  <div v-bind="objectOfAttrs">abc</div>
  <p v-if="seen">Now you see me</p>
  <p v-show="seen">Now you see me</p>
  <a :href="google">Google</a> <br>
  <button v-on:click="clickMe">Click Me</button>
</template>

<style scoped>

</style>
