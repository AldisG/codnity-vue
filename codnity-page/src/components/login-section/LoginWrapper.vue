<script setup lang="ts">
import { defineComponent } from "vue";
import Button from "../utility/Button.vue";
defineComponent({
  Button,
});
const onSubmitHandler = (e: Event) => {
  e.preventDefault();
  // console.log(e.target[0].value);
};
</script>

<template>
  <div class="content-wrappers">
    <div class="login--header">
      <h1>Welcme back!</h1>
      <span>Please login to your account.</span>
    </div>
    <form class="login--form" @submit="onSubmitHandler">
      <input type="email" name="email" id="email" required />
      <input type="password" name="password" id="password" required />
      <div class="login--options-wrapper">
        <input
          type="checkbox"
          name="keep-me-logged-in"
          id="keep-me-logged-in"
        />
        <div class="login--forgot-password">Forgot password?</div>
      </div>
      <Button :accentedButton="true" text="Log in" />
    </form>
  </div>
</template>

<style></style>
