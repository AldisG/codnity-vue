<template>
  <div class="welcome--create-account">
    <h6 class="welcome--sub-header">Not a member yet?</h6>
    <span class="welcome--sub-header-info">
      Please use your personal and company information to Create Account
    </span>
    <div class="position-flex-center">
      <Button text="Create Account" :accentedButton="false" />
    </div>
  </div>
</template>

<script lang="ts">
import Button from "../utility/Button.vue";

export default {
  name: "WelcomeCreateAccount",
  components: { Button },
};
</script>

<style>
.welcome--create-account {
  display: grid;
  gap: 1rem;
}
.welcome--sub-header {
  font-size: 16px;
  font-weight: normal;
}
.welcome--sub-header-info {
  font-size: 12px;
  font-weight: normal;
}
</style>
