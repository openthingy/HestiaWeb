<script setup lang="ts">
import NavBar from "@/components/NavBar.vue";
import SideBar from "@/components/SideBar.vue";
</script>

<template>
    <SideBar/>
    <NavBar/>
    <v-main class="mx-3 my-3">
      <v-sheet class="rounded-lg">
        <div class="mx-3">
          <h2>Declaração Periodica de IVA</h2>
          <v-text-field
          class="mt-3"
          label="Input 1"
          ></v-text-field>
        </div>
      </v-sheet>
    </v-main>
</template>

<script lang="ts">

</script>