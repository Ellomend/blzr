<script setup lang="ts">
import { ref } from 'vue';
import './3d.ts';
const todos = ref<{ id: number; content: string }[]>([
  {
    id: 1,
    content: 'ct1',
  },
]);

</script>

<template>
  <div>
    <q-card class="my-card">
      <q-card-section>
        <div class="text-h6">Our Changing Planet</div>
        <div class="text-subtitle2">by John Doe</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam quod
        voluptates, quia, voluptate, voluptas quas voluptatum quae quibusdam
        doloremque quidem quos. Quisquam, quae. Quisquam, quae. Quisquam, quae.

        <span style="color: red">{{ todos }}</span>
        <q-btn
          class="q-ml-md"
          color="primary"
          label="Read more"
          icon="chevron_right"
          size="sm"
          flat
          dense
        />
      </q-card-section>
    </q-card>
  </div>
</template>

<style lang="scss"></style>
