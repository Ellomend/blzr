<template>
  <q-page class="q-ma-md">
    <q-card
      class="my-card text-white shadow-10"
      style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)"
    >
      <q-card-section>
        <div class="text-h6">Our Changing Planet</div>
        <div class="text-subtitle2">by John Doe</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ todos }}
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <q-card-section>
        <div class="text-h6">Our Changing Planet</div>
        <div class="text-subtitle2">by John Doe</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ todos }}
      </q-card-section>
    </q-card>
    <demo-todo />
  </q-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import DemoTodo from '../components/TodoContainer/DemoTodo.vue';

const todos = ref<{ id: number; content: string }[]>([
  {
    id: 1,
    content: 'ct1',
  },
]);
</script>
