<script setup lang="ts">
import { defineComponent } from "vue";
import Button from "../utility/Button.vue";
import Checkbox from "../utility/Checkbox.vue";
defineComponent({
  Button,
  Checkbox,
});
const typedInputList = ["email", "password"];
const onSubmitHandler = (e: Event) => {
  e.preventDefault();
  // console.log(e.target[0].value);
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
        <input
          :type="item"
          :name="item"
          :id="item"
          required
          :placeholder="item.toUpperCase()"
        />
      </div>
      <div class="login--options-wrapper">
        <Checkbox />
        <div class="login--forgot-password">Forgot password?</div>
      </div>
      <Button :accentedButton="true" text="Log in" />
    </form>
  </div>
</template>

<style>
.login--content {
  width: 100%;
  margin: 0 auto;
  padding: 0 60px;
  padding-top: var(--vt-welcome-top-padding);
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
  gap: 4px;
}
input {
  margin-bottom: 14px;
  color: var(--vt-c-dark);
}
#email,
#password {
  width: 100%;
  padding: 8px;
  font-size: 14px;
}
.login--forgot-password {
  color: var(--vt-c-black);
  font-size: 14px;
  font-weight: 500;
  position: relative;
  width: max-content;
}
.login--forgot-password::after {
  content: "";
  position: absolute;
  width: 100%;
  bottom: -3px;
  left: 0;
  height: 3px;
  background-color: var(--vt-c-accent);
}
</style>
