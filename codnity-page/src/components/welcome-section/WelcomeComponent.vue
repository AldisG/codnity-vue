<script setup lang="ts">
import Logo from "../asset-components/Logo.vue";
import WelcomeCreateAccount from "./WelcomeCreateAccount.vue";
import { ref, onMounted, onUnmounted } from "vue";
const mobileView = ref(false);
const checkScreenWidth = () => {
  const windowsSize = window.innerWidth;
  if (windowsSize >= 800) {
    mobileView.value = true;
  } else {
    mobileView.value = false;
  }
};
onMounted(() => {
  window.addEventListener("resize", checkScreenWidth);
});
onUnmounted(() => {
  window.removeEventListener("resize", checkScreenWidth);
});
const desktopHeader = "Your Produc Our Priority, Shipping made simple.";
const mobileHeader =
  "Built for Logistics Professionals, Perfected for Your Business";
</script>

<template>
  <div class="welcome--container">
    <div class="welcome-and-login-wrapper blank-filter">
      <div class="welcome--content-wrapper">
        <Logo />
        <h2 v-if="mobileView" class="welcome--main-header">
          {{ desktopHeader }}
        </h2>
        <h2 v-else class="welcome--main-header">
          {{ mobileHeader }}
        </h2>
        <WelcomeCreateAccount />
      </div>
    </div>
  </div>
</template>

<style>
.welcome--container {
  background-image: url("../../assets/visual/background-for-logo.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 100vh;
  margin: 0 auto;
  overflow: hidden;
  color: var(--vt-c-white);
}
.blank-filter {
  background-color: #333333cc;
  width: 100%;
  height: 100vh;
}
.welcome--content-wrapper {
  display: grid;
  align-content: center;
  margin: 0 auto;
  max-width: 1000px;
  gap: 14px;
}
</style>
