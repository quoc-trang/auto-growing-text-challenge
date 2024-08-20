<script setup>
import { ref, watch } from "vue";
const modelValue = defineModel();
const el = ref();

watch(modelValue, () => {
  el.value.style.height = "auto";
  el.value.style.height = el.value.scrollHeight + "px";
});
</script>
<template>
  <textarea v-model="modelValue" ref="el" rows="1"></textarea>
</template>
