<template>
  <CSSProvider :config="import('./master.css')">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </CSSProvider>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";
const CSSProvider = defineAsyncComponent(
  async () => (await import("@master/css.vue")).CSSProvider
);
</script>
