<template>
  <div class="max-w-screen-xl mx-auto px-2 lg:px-0 pt-4 pb-20">
    <p class="text-green-500 text-xl">This is about page!</p>
    <p class="text-gray-500">{{ data.content }}</p>
  </div>
</template>

<script setup>
  const {data} = await useFetch("/api/about")
</script>