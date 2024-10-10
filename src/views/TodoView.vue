<script setup>
import { ref } from 'vue'

// Reactive array to store todos
const todos = ref([])

// Reactive variable for new todo input
const newTodo = ref('')

// Add new todo
const addTodo = () => {
  if (newTodo.value.trim() !== '') {
    todos.value.push({
      id: Date.now(),
      text: newTodo.value,
      editing: false,
    })
    newTodo.value = '' // Clear input after adding
  }
}

// Delete todo
const deleteTodo = (id) => {
  todos.value = todos.value.filter(todo => todo.id !== id)
}

// Edit todo
const editTodo = (todo) => {
  todo.editing = true
}

// Save edited todo
const saveTodo = (todo) => {
  if (todo.text.trim() !== '') {
    todo.editing = false
  }
}
</script>

<template>
  <div>
    <h1>Todo List</h1>

    <!-- Add new todo -->
    <input v-model="newTodo" placeholder="Add a new todo" />
    <button @click="addTodo">Add Todo</button>

    <!-- Todo list -->
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <div v-if="!todo.editing">
          {{ todo.text }}
          <button @click="editTodo(todo)">Edit</button>
          <button @click="deleteTodo(todo.id)">Delete</button>
        </div>
        <div v-else>
          <input v-model="todo.text" />
          <button @click="saveTodo(todo)">Save</button>
        </div>
      </li>
    </ul>
  </div>
</template>
