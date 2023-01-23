<template>
  <label class="input-label">
    <div
      :class="`floating-label ${!inputText ? '' : 'hide-label'} ${
        inputFocused ? 'focused' : ''
      }`"
    >
      {{ inputType }}
    </div>
    <input
      :type="inputType"
      :name="inputType"
      :id="inputType"
      :onfocus="handleFocus"
      :onblur="handleBlur"
      required
      v-model="inputText"
      :minlength="inputType == 'password' ? 6 : 0"
    />
  </label>
</template>

<script setup lang="ts">
import { defineProps, ref } from "vue";
defineProps({
  inputType: String,
});
const inputText = ref("");
const inputFocused = ref(false);

const handleFocus = () => {
  inputFocused.value = true;
};
const handleBlur = () => {
  inputFocused.value = false;
};
</script>

<style>
.input-label {
  display: block;
  margin-bottom: 14px;
  color: var(--vt-c-dark);
  position: relative;
}
.floating-label {
  background-color: var(--vt-c-white);
  opacity: 1;
  padding: 4px;
  position: absolute;
  top: 3px;
  left: 4px;
  padding: 2px 4px;
  z-index: 2;
  transition: top 0.3s, opacity 0.3s, font-weight 0.3s, font-size 0.3s;
  font-size: 18px;
  font-weight: bold;
  user-select: none;
  pointer-events: none;
}
.floating-label.focused {
  top: -10px;
  font-size: 12px;
  padding: 1px 2px;
  font-weight: normal;
}
.hide-label {
  opacity: 0;
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
