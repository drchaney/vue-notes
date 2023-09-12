<!--
Here we show the simplest possible component which accepts a prop and renders it.
Learn more about components in the guide!
-->

<script setup>
import { ref } from 'vue'
import TodoItem from './TodoItem.vue'

const burritoList = ref([
  { id: 0, text: 'Chicken' },
  { id: 1, text: 'Cheese' },
  { id: 2, text: 'Breakfast' }
])
</script>

<template>
  <ol>
    <!--
      We are providing each todo-item with the todo object
      it's representing, so that its content can be dynamic.
      We also need to provide each component with a "key",
      which is explained in the guide section on v-for.
    -->
    <TodoItem
      v-for="burrito in burritoList"
      :todo="burrito"
      :key="burrito.id"
    ></TodoItem>
  </ol>
</template>
