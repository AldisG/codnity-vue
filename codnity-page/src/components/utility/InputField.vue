<template>
  <input
    :type="inputType"
    :name="inputType"
    :id="inputType"
    required
    :placeholder="inputType?.toUpperCase()"
  />
</template>
<script setup lang="ts">
import { defineProps } from "vue";
defineProps({
  inputType: String,
});
</script>
<style>
input {
  margin-bottom: 14px;
  color: var(--vt-c-dark);
}
#email,
#password {
  width: 100%;
  padding: 8px;
  font-size: 14px;
  border: none;
  outline: 1px solid var(--vt-c-dark);
  border-radius: 4px;
}
</style>
