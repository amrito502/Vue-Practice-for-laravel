<script setup>
import {reactive, ref, computed} from 'vue'

const todo = ref("")

const todos = reactive([
  {
    id: 1,
    title: "Todo One",
    completed: false
  },
  {
    id: 2,
    title: "Todo Two",
    completed: true
  },
  {
    id: 3,
    title: "Todo Three",
    completed: false
  },
])

const addTodo = (index) => {
  if(todo.value === ''){
    return
  }

  todos.push({
    id: todos.length + 1,
    title: todo.value,
    completed: false

  })

  todo.value = ""
}

const checkComplete = (index) => {
  todos[index].completed = !todos[index].completed
}

const removeTodo = (index) => {
  todos.splice(index, 1)
}

const countAllTodo = computed(() => {
  return todos.length
})

const countCompletedTodo = computed(() => {
  return todos.filter(todo => todo.completed).length
})

</script>

<template>
  <div
    class="max-w-md mx-auto bg-white shadow-lg rounded-lg overflow-hidden mt-16 border p-6"
  >
    <div class="text-2xl uppercase text-gray-700 font-bold">Todo List ({{countCompletedTodo}} /{{ countAllTodo }})</div>
    <div>
      <form @submit.prevent="addTodo">
        <div class="flex items-center border-b-2 border-teal-500 py-2">
          <input v-model="todo"
            class="border-none focus:outline-none text-gray-700"
            type="text"
            placeholder="Add a task"
          />
          <button
            class="ml-auto flex-shrink-0 bg-teal-500 hover:bg-teal-700 border-4 text-sm hover:border-teal-700 text-white py-1 px-2 rounded"
            type="submit"
          >
            Add
          </button>
        </div>
      </form>
    </div>

    <div v-for="(todo, index) in todos" :key="todo.id" class="flex items-center justify-between mt-5">
      <div  class="flex items-center justify-between">
        <input @input="checkComplete(index)" :checked="todo.completed"
        :id="`todo-${todo.id}`"
          class="h-4 w-4 text-teal-600 focus:ring-teal-500 border-gray-300 rounded"
          type="checkbox"
          name="todo"
        />

        <label class="ml-3 block text-gray-900" :class="{'line-through' : todo.completed}" :for="`todo-${todo.id}`"
          ><span class="text-lg font-medium">{{todo.title}}</span></label
        >
        
      </div>
      <div>
        <button @click="removeTodo(index)" class="flex-shrink-0 border-t-neutral-400 text-white bg-red-700 py-1 px-2 rounded">Delete</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
