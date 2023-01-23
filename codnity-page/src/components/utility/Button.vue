<template>
  <button :class="`button ${accentedButton ? 'accented' : ''}`">
    {{ text }}
  </button>
</template>

<script setup lang="ts">
defineProps({
  text: String,
  accentedButton: Boolean,
});
</script>

<style>
.button {
  margin-top: 8px;
  font-size: 14px;
  font-weight: normal;
  padding: 10px 20px;
  outline: 1px solid var(--vt-c-white);
  color: var(--vt-c-white);
  background-color: transparent;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  width: max-content;
  transition: all 0.3s;
}
.button:hover,
.button:active,
.button:focus {
  background-color: var(--vt-c-white-transparent);
}
.accented {
  background-color: var(--vt-c-accent);
  color: var(--vt-c-black);
  outline: 1px solid transparent;

  outline: none;
  padding: 10px 42px;
  transition: all 0.2s;
}
.accented:hover,
.accented:active,
.accented:focus {
  outline: none;
  background-color: var(--vt-c-accent);
  outline: 1px solid var(--vt-c-black);
}
</style>
