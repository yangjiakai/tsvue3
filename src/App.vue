<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import CustomizationPanel from "./components/CustomizationPanel.vue";
import NavigationDrawer from "./components/NavigationDrawer.vue";
import AppBar from "./components/AppBar.vue";
import { useCustomizationStore } from "@/stores/customization";

const customization = useCustomizationStore();
</script>

<template>
  <v-app :theme="customization.darkTheme ? 'dark' : 'light'">
    <AppBar />
    <NavigationDrawer />
    <CustomizationPanel />
    <v-main>
      <RouterView />
    </v-main>
    <div class="wrapper">
      <nav></nav>
    </div>
  </v-app>
</template>

<style scoped></style>
