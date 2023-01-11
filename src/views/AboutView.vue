<template>
  <div class="about">
    <h1>This is an about page</h1>
    <v-btn color="success">text</v-btn>
    {{ str2 }}
    <v-divider></v-divider>
    {{ e1 }} | {{ e2 }}|{{ h1 }}
    <v-checkbox
      hide-details
      v-model="customiztion.darkTheme"
      label="Mini"
    ></v-checkbox>
  </div>
</template>

<script setup lang="ts">
import { ref, reactive } from "vue";
import { useCustomizationStore } from "@/stores/customization";

const customiztion = useCustomizationStore();

const num1 = ref<number>();
const str1 = ref<string>("str");
const str2 = ref<number | string>("str2");

interface User {
  name: string;
  age: number;
  email: string;
  about: string;
}

const user: User = reactive({
  name: "",
  age: 0,
  email: "",
  about: "",
});

enum YesNo {
  Yes = 3,
  No = 4,
}

enum HttpRequestField {
  "Accept",
  "Accept-Charset",
  "Accept-Datetime",
  "Accept-Encoding",
  "Accept-Language",
}

const h1 = ref(HttpRequestField.Accept);

const e1 = ref(YesNo.Yes);
const e2 = ref(YesNo.No);
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
