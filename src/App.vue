<script setup lang="ts">
import AutoHeightTextarea from "./components/AutoHeightTextarea.vue";
import { useCycleList } from "@vueuse/core";
import data from "./assets/data.json";
const { state, next } = useCycleList(data);
</script>
<template>
  <div class="page">
    <div class="min-w-96">
      <AutoHeightTextarea v-model="state" />

      <button @click="next()">Random Message</button>
    </div>
  </div>
</template>
