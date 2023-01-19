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
  <div class="welcome-and-login-wrapper login--content">
    <div class="login--headers">
      <h1>Welcme back!</h1>
      <span>Please login to your account.</span>
    </div>
    <form class="login--form" @submit="onSubmitHandler">
      <input
        type="email"
        name="email"
        id="email"
        required
        placeholder="EMAIL"
      />
      <input
        type="password"
        name="password"
        id="password"
        required
        placeholder="PASSWORD"
      />
      <div class="login--options-wrapper">
        <input
          type="checkbox"
          name="keep-me-logged-in"
          id="keep-me-logged-in"
          checked
        />
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
}
.login--headers {
  padding-bottom: 32px;
  display: grid;
  gap: 8px;
}
.login--form {
  display: grid;
  gap: 4px;
}
input {
  margin-bottom: 14px;
}
#email,
#password {
  width: 100%;
  padding: 8px;
  font-size: 14px;
}
</style>
