<script setup>
</script>

<template>
  <div
    class="max-w-md mx-auto bg-white shadow-lg rounded-lg overflow-hidden mt-16 border p-6"
  >
    <div class="text-2xl uppercase text-gray-700 font-bold">Todo List</div>

    <div>
      <form>
        <div class="flex items-center border-b-2 border-teal-500 py-2">
          <input
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

    <div class="flex items-center justify-between mt-5">
      <div class="flex items-center justify-between">
        <input
          class="h-4 w-4 text-teal-600 focus:ring-teal-500 border-gray-300 rounded"
          type="checkbox"
          name="todo"
          id="todo"
        />
        <label class="ml-3 block text-gray-900" for="todo"
          ><span class="text-lg font-medium">Todo Title</span></label
        >
        
      </div>
      <div>
        <button class="flex-shrink-0 border-t-neutral-400 text-white bg-red-700 py-1 px-2 rounded">Delete</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
