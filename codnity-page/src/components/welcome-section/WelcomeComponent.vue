<script setup lang="ts">
import Logo from "../asset-components/Logo.vue";
import WelcomeCreateAccount from "./WelcomeCreateAccount.vue";
</script>

<template>
  <div class="content-wrappers">
    <Logo />
    <h2 class="welcome--slogan">
      Your Produc Our Priority,<br />
      Shipping made simple.
    </h2>
    <WelcomeCreateAccount />
  </div>
</template>

<style scoped>
.content-wrappers {
  background-image: url("../../assets/visual/background-for-logo.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  overflow: hidden;
}
/* .welcome--slogan */
</style>
