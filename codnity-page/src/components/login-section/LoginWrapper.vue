<script setup lang="ts">
import { defineComponent } from "vue";
import Button from "../utility/Button.vue";
import Checkbox from "../utility/Checkbox.vue";
import InputField from "../utility/InputField.vue";
defineComponent({
  Button,
  Checkbox,
  InputField,
});
const typedInputList = ["email", "password"];

const onSubmitHandler = (e: Event) => {
  e.preventDefault();
};
</script>

<template>
  <div class="welcome-and-login-wrapper login--content">
    <div class="login--headers">
      <h1 class="login--header">Welcme back!</h1>
      <span class="login--subheader">Please login to your account.</span>
    </div>
    <form class="login--form" @submit="onSubmitHandler">
      <div v-for="item in typedInputList" :key="item">
        <InputField :inputType="item" />
      </div>
      <div class="login--options-wrapper">
        <Checkbox />
        <div class="login--forgot-password">Forgot password?</div>
      </div>
      <div class="position-flex-end">
        <Button :accentedButton="true" text="Log in" />
      </div>
    </form>
  </div>
</template>

<style>
.login--content {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
  color: var(--vt-c-dark);
}
.login--headers {
  padding-bottom: 32px;
  display: grid;
  gap: 8px;
}
.login--header {
  font-size: 32px;
}
.login--subheader {
  font-size: 14px;
}
.login--form {
  display: grid;
  gap: 8px;
}
.login--options-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 12px;
}

.login--forgot-password {
  color: var(--vt-c-black);
  font-size: 14px;
  font-weight: 500;
  position: relative;
  width: max-content;
  cursor: pointer;
  user-select: none;
}
.login--forgot-password::after {
  content: "";
  position: absolute;
  width: 100%;
  bottom: -3px;
  left: 0;
  height: 1px;
  background-color: var(--vt-c-accent);
  transition: height 0.3s;
}
.login--forgot-password:hover::after {
  height: 3px;
}
.position-flex-end {
  justify-self: flex-end;
}
</style>
