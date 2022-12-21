<script setup>
const experiences = [
  {
    title: "Web Development & UI/UX Specialist",
    company: "Yopaat",
    imageURL: "/img/yopaat.jpg",
    work_type: "Full Time",
    work_time: "1.2 year",
  },
  {
    title: "Web Development & UI/UX Specialist",
    company: "Artapot",
    imageURL: "/img/artapot.jpg",
    work_type: "Full Time",
    work_time: "9 months",
  },
  {
    title: "Web Development & UI/UX Specialist",
    company: "Uskudar University",
    imageURL: "/img/uskudar.jpg",
    work_type: "Full Time",
    work_time: "1.7 year",
  },
  {
    title: "Web Developer",
    company: "Pandary Software",
    imageURL: "/img/panda.jpg",
    work_type: "Full Time",
    work_time: "1.6 year",
  },
  {
    title: "Technical Support Specialist, Web Developer",
    company: "Netservis",
    imageURL: "/img/netservis.jpg",
    work_type: "Full Time",
    work_time: "3.2 years",
  },
  {
    title: "Technical Support Specialist",
    company: "Hewlett-Packard",
    imageURL: "/img/hp.jpg",
    work_type: "Full Time",
    work_time: "1.5 year",
  },
];
</script>

<template>
  <div class="bg-gray-800 pt-6 pb-8 px-8 rounded">
    <div class="flex items-center justify-between border-b mb-4 pb-2.5 border-gray-700">
      <h2 class="uppercase text-xs text-gray-400">experiences</h2>
    </div>

    <ul
      class="space-y-2.5 max-h-96 overflow-y-scroll scrollbar-thin scrollbar-track-gray-900 scrollbar-thumb-gray-700 pr-6">
      <li class="p-4 rounded bg-gray-800 brightness-90 flex space-x-4 items-center" v-for="experience in experiences"
        :key="experience.title">
        <img :src="experience.imageURL" class="w-12 h-12 rounded-full object-cover p-1 bg-white" alt="" />

        <div>
          <h2 class="font-medium text-gray-300 text-sm">
            {{ experience.title }}
          </h2>
          <p class="text-sm text-gray-500">
            {{ experience.company }} · {{ experience.work_type }} ·
            {{ experience.work_time }}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
