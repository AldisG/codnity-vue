<script setup lang="ts">
import Logo from "../asset-components/Logo.vue";
import WelcomeCreateAccount from "./WelcomeCreateAccount.vue";
</script>

<template>
  <div class="welcome--container">
    <div class="welcome-and-login-wrapper blank-filter">
      <div class="welcome--content-wrapper">
        <Logo />
        <h2 class="welcome--slogan">
          Your Produc Our Priority,<br />
          Shipping made simple.
        </h2>
        <WelcomeCreateAccount />
      </div>
    </div>
  </div>
</template>

<style scoped>
.welcome--container {
  background-image: url("../../assets/visual/background-for-logo.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  margin: 0 auto;
  overflow: hidden;
  color: #fff;
}
.blank-filter {
  background-color: #333333cc;
  width: 100%;
  height: 100vh;
}
.welcome--content-wrapper {
  max-width: var(--vt-welcome-size);
  display: grid;
  margin: 0 auto;

  gap: 2rem;
}
/* .welcome--slogan */
</style>
