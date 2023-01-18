<script setup lang="ts">
import WelcomeComponent from "@/components/WelcomeComponent.vue";
import LoginWrapper from "@/components/LoginWrapper.vue";
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
@media screen and (max-width: 412px) {
  .login-wrapper {
    grid-template-columns: 1fr;
  }
}
</style>
