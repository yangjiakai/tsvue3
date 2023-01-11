<script setup lang="ts">
import { useCustomizationStore } from "@/stores/customization";
const customization = useCustomizationStore();
</script>

<template>
  <div>
    <v-navigation-drawer permanent location="right">
      <template v-slot:prepend>
        <v-list-item
          lines="two"
          prepend-avatar="https://randomuser.me/api/portraits/women/81.jpg"
          title="Jane Smith"
          subtitle="Logged in"
        ></v-list-item>
      </template>

      <v-divider></v-divider>
      <div class="ml-5 pa-5">
        <v-switch
          v-model="customization.darkTheme"
          label="主题"
          color="orange"
          hide-details
        ></v-switch>
      </div>
      <v-divider></v-divider>
      <v-btn
        color="primary"
        @click.stop="
          customization.SET_MINI_SIDEBAR(!customization.mini_sidebar)
        "
        >mini sidebar</v-btn
      >
    </v-navigation-drawer>
  </div>
</template>

<style scoped></style>
