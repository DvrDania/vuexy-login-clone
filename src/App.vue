<script setup>
import LoginForm from "./components/LoginForm.vue";
import Logo from "./components/Logo.vue";
</script>

<template>
  <main>
    <div class="relative flex items-center justify-center bg-gray-50">
      <div class="absolute top-8 left-8 flex items-center">
        <p class="mr-3 text-2xl font-semibold text-violet-600">Vuexy</p>
        <Logo class="text-violet-600" />
      </div>
      <img id="login-img" alt="login-img" src="./assets/images/login-img.svg" />
    </div>
    <LoginForm class="flex flex-col justify-center p-20" id="login-form" />
  </main>
</template>

<style lang="postcss">
#app {
  @apply font-montserrat;
}
main {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-template-rows: 1fr;
  grid-template-areas: "img form";
}
.login-img {
  grid-area: img;
}
.login-form {
  grid-area: form;
}
</style>
