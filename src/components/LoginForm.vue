<script setup>
import { ref } from "vue";
import HelpIcon from "vue-material-design-icons/HelpCircleOutline.vue";
import PassIconShow from "vue-material-design-icons/EyeOutline.vue";
import PassIconHide from "vue-material-design-icons/EyeOffOutline.vue";
import Github from "vue-material-design-icons/Github.vue";
import Twitter from "vue-material-design-icons/Twitter.vue";
import Email from "vue-material-design-icons/EmailOutline.vue";
import Facebook from "vue-material-design-icons/Facebook.vue";

const passVisible = ref(false);
</script>
<template>
  <form class="accent-violet-500" dir="rtl" action="">
    <h1 class="text-2xl font-medium text-slate-600">Welcome to Vuexy! 👋</h1>
    <p class="mt-4 text-sm text-slate-500">
      Please sign-in to your account and start the adventure
    </p>
    <div
      class="relative mt-6 rounded-md bg-violet-100 p-4 font-normal text-violet-500"
    >
      <HelpIcon :size="20" class="absolute left-2 top-2" />
      <small class="block"
        ><span class="font-medium">Admin</span>: admin@demo.com | admin</small
      >
      <small class="mt-1 block"
        ><span class="font-medium">Client</span>: client@demo.com |
        client</small
      >
    </div>
    <div class="input-group flex flex-col">
      <label for="email">Email</label>
      <input
        class="mt-1 rounded-md border border-violet-200 p-1.5 px-4 text-sm text-slate-700 outline-none transition-all placeholder:text-slate-400 focus:border-violet-600 focus:ring-2 focus:ring-violet-200"
        type="email"
        name="email"
        id="email"
        placeholder="admin@demo.com"
      />
    </div>
    <div class="input-group flex flex-col">
      <div class="flex items-end justify-between">
        <label for="password">Password</label>
        <a href="#" class="text-xs text-violet-500 hover:text-violet-600"
          >Forgot Passowrd?</a
        >
      </div>
      <div class="relative w-full">
        <PassIconShow
          v-if="!passVisible"
          class="absolute left-4 top-1/2 mt-0.5 -translate-y-1/2 cursor-pointer text-slate-400"
          :size="17"
          @click="passVisible = true"
        />
        <PassIconHide
          v-if="passVisible"
          class="absolute left-4 top-1/2 mt-0.5 -translate-y-1/2 cursor-pointer text-slate-400"
          :size="17"
          @click="passVisible = false"
        />
        <input
          class="mt-1 w-full rounded-md border border-violet-200 p-1.5 px-4 text-slate-700 outline-none transition-all placeholder:text-slate-400 focus:border-violet-600 focus:ring-2 focus:ring-violet-200"
          :type="passVisible ? 'text' : 'password'"
          name="password"
          id="password"
        />
      </div>
    </div>
    <div class="mt-3 flex items-center">
      <input
        type="checkbox"
        name="remember"
        id="remember"
        class="h-3.5 w-3.5 border-violet-200 outline-none"
      />
      <label class="mr-2 mb-px" for="remember">Remember me</label>
    </div>
    <input
      class="mt-3 cursor-pointer rounded-md bg-violet-500 p-3 text-sm font-medium text-white transition-all hover:shadow-lg hover:shadow-violet-500/40 active:bg-violet-600"
      type="submit"
      value="Sign in"
    />
    <p class="py-4 text-center text-sm font-light">
      New on our platform?
      <a href="#" class="text-violet-500 hover:text-violet-600"
        >Create an account</a
      >
    </p>
    <div class="flex items-center justify-center gap-4">
      <span class="block h-px w-1/3 bg-slate-300"></span>
      <span class="mb-0.5 text-sm font-light">or</span>
      <span class="block h-px w-1/3 bg-slate-300"></span>
    </div>
    <div class="mt-4 flex flex-row-reverse justify-center gap-4">
      <div class="rounded-md bg-[#333] p-1.5 text-white">
        <Github :size="20" />
      </div>
      <div class="rounded-md bg-[#ea4335] p-1.5 text-white">
        <Email :size="20" />
      </div>
      <div class="rounded-md bg-[#1da1f2] p-1.5 text-white">
        <Twitter :size="20" />
      </div>
      <div class="rounded-md bg-[#1877f2] p-1.5 text-white">
        <Facebook :size="20" />
      </div>
    </div>
  </form>
</template>

<style lang="postcss" scoped>
.input-group {
  @apply mt-4;
}
label {
  @apply text-sm font-light text-slate-600;
}
</style>
