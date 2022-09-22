<script setup>
const brands = [
  {
    name: "Vue JS",
    logo: "/img/vue.png",
    link: "https://vuejs.org/",
  },
  {
    name: "Nuxt JS",
    logo: "/img/nuxt.png",
    link: "https://nuxtjs.org/",
  },
  {
    name: "React JS",
    logo: "/img/react.png",
    link: "https://reactjs.org/",
  },
  {
    name: "Vite",
    logo: "/img/vite.png",
    link: "https://vitejs.dev/",
  },
  {
    name: "Node JS",
    logo: "/img/nodejs.png",
    link: "https://nodejs.org/en/",
  },
  {
    name: "Tailwind CSS",
    logo: "/img/tailwind.png",
    link: "https://tailwindcss.com/",
  },
  {
    name: "SASS",
    logo: "/img/sass.png",
    link: "https://sass-lang.com/",
  },
  {
    name: "Adobe XD",
    logo: "/img/adobexd.png",
    link: "https://www.adobe.com/tr/products/xd.html",
  },
  {
    name: "HTML5",
    logo: "/img/html5.png",
    link: "https://tr.wikipedia.org/wiki/HTML5",
  },
  {
    name: "GSAP",
    logo: "/img/gsap.svg",
    link: "https://greensock.com/gsap/",
  },
  {
    name: "Supabase",
    logo: "/img/supabase.png",
    link: "https://supabase.com/",
  },
  {
    name: "Docker",
    logo: "/img/docker.webp",
    link: "https://www.docker.com/",
  },
];
</script>

<template>
  <div class="grid grid-cols-4 md:flex items-center justify-center space-x-2">
    <a
      v-for="brand in brands"
      :key="brand.name"
      :href="brand.link"
      :title="brand.name"
      class="p-4 hover:bg-gray-800 rounded"
      target="_blank"
    >
      <img :src="brand.logo" class="w-8" :alt="brand.name"
    /></a>
  </div>
</template>
