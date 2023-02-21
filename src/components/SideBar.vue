<script setup lang="ts">
import { ref } from "vue";
</script>

<template>
    <v-navigation-drawer v-model="drawer">
    </v-navigation-drawer>
</template>

<script lang="ts">
const drawer = ref(null);
</script>