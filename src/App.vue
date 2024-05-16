<script setup>
import { ref, reactive } from "vue";
// let name = ref("Amrito Bosu")

// let email = ref("");
// let password = ref("");

const form = reactive({
  email: "",
  password: ""
})

</script>

<template>
  <div>
    <!-- <input type="text" v-model="name"><br> -->
    <!-- <p>{{ name }}</p> -->

    <form action="">
      <input type="text" v-model="form.email" name="email" placeholder="Enter Email" /><br />
      <br />
      <input type="text" v-model="form.password" name="password" placeholder="Enter Password" />
    </form>
    {{ form.email }} / {{ form.password }}
  </div>
</template>

<style scoped>
</style>
