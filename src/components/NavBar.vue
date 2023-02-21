<script setup lang="ts">
import { ref } from 'vue'
import { name } from "./info.json";
const appName = ref(name);
</script>

<template>

    <v-app-bar flat>
      
      <v-container class="fill-height d-flex align-center">
        <v-toolbar-title>{{ appName }}</v-toolbar-title>
          
        <v-btn
          v-for="link in links"
          :key="link.name"
          :href="link.link"
          variant="text"
        >
          {{ link.name }}
        </v-btn>

        <v-avatar
          class="me-10 ms-4"
          color="grey-darken-1"
          size="32"
        ></v-avatar>

        
      </v-container>
    </v-app-bar>

</template>

<script lang="ts">
const links = ref([
  {
    "name": "Dashboard",
    "link": "/link" 
  }
]);
</script>