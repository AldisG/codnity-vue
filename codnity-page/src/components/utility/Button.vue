<template>
  <button>{{ text }}</button>
</template>

<script setup lang="ts">
defineProps({
  text: String,
  accentedButton: Boolean,
});
</script>

<style>
/* dynamic style, unify this button to have adaptive style with 'accentedButton' */
</style>
