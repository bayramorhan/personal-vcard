<script setup>
import { version, devDependencies } from "./package.json";

useHead({
  title: "Orhan Bayram - Personal vCard",
  htmlAttrs: {
    class: "bg-gray-900 h-full overflow-x-hidden",
  },
  bodyAttrs: {
    class:
      "h-full overflow-y-scroll scrollbar-thin scrollbar-track-gray-700 scrollbar-thumb-gray-600 overflow-x-hidden",
  },
});
</script>

<template>
  <div>
    <div class="w-full max-w-5xl mx-auto py-4 px-4 lg:px-0 lg:py-10 space-y-10">
      <section class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <profile-card />
        <skill-card />
      </section>
      <section>
        <brand-list />
      </section>
      <section class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <project-card />
        <experience-card />
      </section>
      <footer class="pb-6 text-xs text-gray-500 text-center space-y-2">
        <p>
          ©2021-2022 All Rights Reserved. &middot; This website does not use any
          cookies
        </p>
        <p>
          App Version {{ version }} &middot; Nuxt Version
          {{ devDependencies.nuxt }}
        </p>
      </footer>
    </div>
  </div>
</template>
