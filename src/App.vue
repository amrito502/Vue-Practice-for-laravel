<script setup>
import { ref, computed } from "vue";

const password = ref("");

const passwordStrength = computed(() => {
  let strength = (password.value.length * 100) / 10;
  return Math.min(strength, 100);
});

let firstName = ref("");
let lastName = ref("");

const fullName = computed(() => {
  let fullName = firstName.value + " " + lastName.value;
  return fullName;
});
</script>

<template>
  <div>
    <input
      type="password"
      v-model="password"
      placeholder="Enter Your Password"
    />
    {{ passwordStrength }}<span>% Strong</span>
    <hr />
    <input type="text" v-model="firstName" placeholder="Enter Your firstName" />
    <input type="text" v-model="lastName" placeholder="Enter Your lastName" />
    {{ fullName }}
  </div>
</template>

<style scoped>
</style>
