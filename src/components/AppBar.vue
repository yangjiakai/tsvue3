<script setup lang="ts">
import { useCustomizationStore } from "@/stores/customization";
const customization = useCustomizationStore();
</script>

<template>
  <div>
    <v-app-bar title="Application">
      <v-btn to="/" color="info">Home</v-btn>
      <v-btn to="/about" color="info">About</v-btn>
    </v-app-bar>
  </div>
</template>

<style scoped></style>
