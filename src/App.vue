<script setup>
import {ref, onMounted, onUpdated} from 'vue'

const users = ref([])

function getUsers(){
  users.value = [
    {
      id: 1,
      name: "Amrito Bosu"
    },
     {
      id: 2,
      name: "Sakib"
    },
  ]
}

onMounted(() => {
  getUsers()
})

onUpdated(() => {

})

</script>

<template>
  <div>
    <div v-for="user in users" :key="user.id">{{user.name}}</div>
  </div>
</template>

<style scoped>

</style>
