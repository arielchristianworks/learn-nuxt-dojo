<template>
  <div class="card h-full">
    <div class="card-media">
      <img :src="product.image" :alt="product.title" :title="product.title">
    </div>
    <div class="card-content">
      <p class="text-lg">{{ product.title }}</p>
      <p class="text-sm text-gray-500 truncate" :title="product.description">{{ product.description }}</p>
    </div>
    <div class="card-actions">
      <NuxtLink class="text-green-500" :to="`/products/${product.id}`">View more &raquo;</NuxtLink>
    </div>
  </div>
</template>

<script setup>
  const {product} = defineProps(['product'])
  console.log(product);
</script>