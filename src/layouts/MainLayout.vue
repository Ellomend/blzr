<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Quasar App </q-toolbar-title>

        <div>
          <!-- link to home page -->
          <q-btn
            flat
            dense
            round
            icon="home"
            aria-label="Home"
            :to="{ name: 'home' }"
          />
          <!-- link to demo page -->
          <q-btn
            flat
            dense
            round
            icon="list"
            aria-label="Demo"
            :to="{ name: 'demo' }"
          />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
