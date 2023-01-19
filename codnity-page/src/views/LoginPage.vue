<script setup lang="ts">
import LoginWrapper from "../components/login-section/LoginWrapper.vue";
import WelcomeComponent from "../components/welcome-section/WelcomeComponent.vue";
</script>

<template>
  <div class="login-wrapper">
    <WelcomeComponent />
    <LoginWrapper />
  </div>
</template>

<style>
.login-wrapper {
  width: 100%;
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
@media screen and (max-width: 800px) {
  .login-wrapper {
    grid-template-columns: 1fr;
  }
}
</style>
