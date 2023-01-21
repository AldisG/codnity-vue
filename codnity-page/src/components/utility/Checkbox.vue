<template>
  <label class="container">
    Keep me logged in
    <input type="checkbox" name="keep-me-logged-in" id="keep-me-logged-in" />
    <span class="checkmark"></span>
  </label>
</template>

<script lang="ts">
export default {};
</script>

<style>
.container {
  display: block;
  position: relative;
  padding-left: 25px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  font-size: 12px;
}
.container:hover {
  text-decoration: underline 1px var(--vt-c-accent);
}

/* Hide the real checkbox */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 14px;
  width: 14px;
  background-color: transparent;
  outline: 2px solid var(--vt-c-accent);
  border-radius: 1px;
}

.container:hover input ~ .checkmark {
  outline: 3px solid var(--vt-c-accent);
}

.container input:checked ~ .checkmark {
  background-color: var(--vt-c-white);
}

.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

.container input:checked ~ .checkmark:after {
  display: block;
}

.container .checkmark:after {
  left: 4px;
  top: 1px;
  width: 5px;
  height: 10px;
  border: solid var(--vt-c-accent);
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>
