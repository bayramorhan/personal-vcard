<script setup>
import { LinkIcon } from '@heroicons/vue/24/outline'

const projects = [
  {
    title: "PUMA Exclusive Design",
    link: "https://bit.ly/puma-exclusive",
    description: 'It\'s an experimental project that I currently working on my free time, with the purpose of improving myself on user interface and user experience. This first version is just the drafts I prepared to determine the way of the design that I want to go with. Next, I plan to turn this design into a real application using a modern javasciprt framework. Main idea; Developing an application that "hypothetically" allows PUMA to bring some of its special collections to the customers and make them shop.'
  }
];
</script>

<template>
  <div class="bg-gray-800 pt-6 pb-8 px-8 rounded">
    <div class="flex items-center justify-between border-b mb-4 pb-2.5 border-gray-700">
      <h2 class="uppercase text-xs text-gray-400">projects</h2>
    </div>

    <ul
      class="space-y-2.5 max-h-96 overflow-y-scroll scrollbar-thin scrollbar-track-gray-900 scrollbar-thumb-gray-700 pr-6">
      <li class="p-4 rounded bg-gray-800 brightness-90 flex space-x-4 items-center" v-for="project in projects"
        :key="project.title">
        <div class="space-y-2.5">
          <h2 class="font-medium text-gray-300 text-sm">
            {{ project.title }}
          </h2>
          <div>
            <p class="text-xs text-gray-400">{{ project.description }}</p>
          </div>
          <div class="space-y-2">
            <p class="text-xs text-amber-500">Live preview doesn't connects to any database. It is just a design
              preview. So there is no login credentials you can just click Sign-In to see the application.</p>
            <nuxt-link :to="project.link" class="text-xs text-sky-500 hover:text-sky-400 inline-flex space-x-2"
              target="_blank" :title="project.title">
              <LinkIcon class="w-3.5" /> <span>Live Preview</span>
            </nuxt-link>

          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
