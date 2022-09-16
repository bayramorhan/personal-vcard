<script setup>
const brands = [
  {
    name: "Vue JS",
    logo: "/img/vue.png",
  },
  {
    name: "Nuxt JS",
    logo: "/img/nuxt.png",
  },
  {
    name: "React JS",
    logo: "/img/react.png",
  },
  {
    name: "Vite",
    logo: "/img/vite.png",
  },
  {
    name: "Node JS",
    logo: "/img/nodejs.png",
  },
  {
    name: "Tailwind CSS",
    logo: "/img/tailwind.png",
  },
  {
    name: "SASS",
    logo: "/img/sass.png",
  },
  {
    name: "Adobe XD",
    logo: "/img/adobexd.png",
  },
  {
    name: "HTML5",
    logo: "/img/html5.png",
  },
  {
    name: "GSAP",
    logo: "/img/gsap.svg",
  },
  {
    name: "Supabase",
    logo: "/img/supabase.png",
  },
  {
    name: "Docker",
    logo: "/img/docker.webp",
  },
];
</script>

<template>
  <div class="grid grid-cols-4 md:flex items-center justify-center space-x-2">
    <a
      v-for="brand in brands"
      :key="brand.name"
      href="#"
      :title="brand.name"
      class="p-4 hover:bg-gray-800 rounded"
      target="_blank"
    >
      <img :src="brand.logo" class="w-8" :alt="brand.name"
    /></a>
  </div>
</template>
