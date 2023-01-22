<template>
  <label class="input">
    <input :type="inputType" :name="inputType" :id="inputType" required />
  </label>
</template>
<script setup lang="ts">
import { defineProps } from "vue";
defineProps({
  inputType: String,
});
</script>
<style>
.input {
  margin-bottom: 14px;
  color: var(--vt-c-dark);
  position: relative;
}
/* Patreiz neiet, laikam INPUT elementam nedrikst but after/before/ add label/div? */
.input::before {
  content: "test";
  background-color: var(--vt-c-white);
  padding: 4px;
  position: absolute;
  top: -1px;
  left: 4px;
  padding: 2px 4px;
  z-index: 2;
}
/* ka targetot parrent, ja click ieks child? */
input:active ­ ~ .input::before {
  content: "test";
  top: -10px;
  left: 4px;
  padding: 2px 4px;
  z-index: 2;
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
#email:hover,
#email:active,
#email:focus,
#password:hover,
#password:active,
#password:focus {
  outline: 2px solid var(--vt-c-dark);
}
</style>
