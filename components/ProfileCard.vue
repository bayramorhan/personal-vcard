<script setup>
import { VideoCameraSlashIcon } from "@heroicons/vue/20/solid";

const showEmail = ref(false);
</script>

<template>
  <div class="bg-gray-800 pb-4 rounded border border-gray-800">
    <div class="flex items-center space-x-4 bg-[#263344] p-4">
      <img src="/img/orhan-bayram.jpg" class="w-14 h-14 rounded-full object-cover" alt="" />
      <div class="flex-1">
        <h2 class="font-semibold text-gray-300 mb-0.5">Orhan Bayram</h2>
        <p class="text-xs text-gray-400">Frontend Developer</p>
      </div>
      <div>
        <ul class="flex items-center space-x-4">
          <li>
            <a href="https://www.linkedin.com/in/bayramorhan/" target="_blank" title="LinkedIn Profile">
              <img src="/img/linkedin.png" class="brightness-75 hover:brightness-100 w-5" alt="" />
            </a>
          </li>
          <li>
            <a href="https://github.com/bayramorhan" target="_blank" title="GitHub Profile">
              <img src="/img/github.png" class="brightness-75 hover:brightness-100 w-5" alt="" />
            </a>
          </li>

          <li class="relative cursor-pointer group">
            <span
              class="bg-black bg-opacity-70 font-medium text-white text-sm px-2 py-2 rounded absolute top-full right-0 mt-2 shadow-lg hidden group-hover:block">trex#7250</span>
            <img src="/img/discord.png" class="brightness-75 hover:brightness-100 w-5" alt="" />
          </li>

          <li>
            <a href="https://steamcommunity.com/id/orhanbayram/" target="_blank" title="Steam Profile">
              <img src="/img/steam.png" class="brightness-75 hover:brightness-100 w-5" alt="" />
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="px-4 pt-4 pb-2">
      <nuxt-link v-if="showEmail" to="mailto:orhanbayram@outlook.com"
        class="text-xs text-sky-500 hover:text-sky-400 cursor-pointer block">orhanbayram@outlook.com</nuxt-link>
      <div v-else class="text-xs text-sky-500 hover:text-sky-400 cursor-pointer" @click="showEmail = true">Show e-mail
        address</div>
    </div>
    <div class="px-4 space-y-6 flex flex-col h-[390px]">
      <p class="text-gray-400 text-sm leading-6">
        Throughout my career, I trained myself mainly on web development and
        improved on this subject. I aim to keep the user experience at a high
        level, and I continue to work on this.
      </p>

      <div class="w-full bg-gray-900 flex-1 flex flex-col items-center justify-center space-y-2.5">
        <template v-if="!showVideo">
          <VideoCameraSlashIcon class="w-10 text-gray-600" />
          <p class="text-gray-600 text-sm">Video is not available yet</p>
        </template>
      </div>
    </div>
  </div>
</template>
