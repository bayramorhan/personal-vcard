<script setup>
import { gsap } from "gsap/dist/gsap";
import { ArrowUturnRightIcon, ArrowPathIcon } from "@heroicons/vue/24/outline";

const tl = gsap.timeline({
  duration: 1,
  width: "50%",
  ease: "bounce.out",
  stagger: 0.5,
});

const isReplaying = ref(false);

const replayHandler = () => {
  isReplaying.value = true;
  tl.restart();
  tl.eventCallback("onComplete", () => {
    isReplaying.value = false;
  });
};

const skills = ref([
  {
    name: "Vue (3.x)",
    progress: 90,
  },
  {
    name: "Nuxt (3.x)",
    progress: 80,
  },
  {
    name: "React",
    progress: 65,
  },
  {
    name: "NodeJS",
    progress: 60,
  },
  {
    name: "Tailwind CSS",
    progress: 100,
  },
  {
    name: "Adobe XD",
    progress: 85,
  },
  {
    name: "HTML5",
    progress: 100,
    increment: 0,
  },
]);

onMounted(async () => {
  await nextTick();
  // skills.value.forEach((skill) => {
  //   skill.increment = skill.progress;
  // });
  tl.fromTo(
    ".progress-bar",
    {
      backgroundColor: "rgb(67, 56, 202)",
    },
    {
      duration: 2,
      width: (index) => {
        return `${skills.value[index].progress}%`;
      },
      backgroundColor: "rgb(22, 163, 74)",
      ease: "slow.out",
      stagger: 0.5,
    }
  );
});
</script>

<template>
  <div class="bg-gray-800 pt-6 pb-8 px-8 rounded">
    <div
      class="flex items-center justify-between border-b mb-4 pb-2.5 border-gray-700"
    >
      <h2 class="uppercase text-xs text-gray-500">skills</h2>

      <div class="flex items-center space-x-4">
        <button
          class="text-gray-500 hover:text-gray-300"
          @click="replayHandler"
        >
          <ArrowPathIcon
            class="w-5"
            :class="{ 'animate-spin text-green-600': isReplaying }"
          />
        </button>
        <button
          class="text-gray-500 hover:text-gray-300 rotate-180"
          @click="tl.reverse()"
        >
          <ArrowUturnRightIcon class="w-5" />
        </button>
      </div>
    </div>

    <ul
      class="h-96 overflow-y-auto scrollbar-thin scrollbar-track-gray-900 scrollbar-thumb-gray-700"
      :class="{ 'pr-6': skills.length > 7 }"
    >
      <li v-for="skill in skills" :key="skill.name" class="py-2.5 space-y-2">
        <p class="text-sm font-medium text-gray-400">
          {{ skill.name }}
        </p>
        <div class="relative">
          <div class="h-1.5 w-full bg-gray-900 rounded-full"></div>
          <div
            class="h-1.5 rounded-full absolute left-0 top-0 progress-bar"
          ></div>
        </div>
      </li>
    </ul>
  </div>
</template>
