<template>
  <div class="min-h-screen max-w-screen-xl mx-auto px-2 lg:px-0 pt-4 pb-20">
    <div class="grid md:grid-cols-3 lg:grid-cols-4 gap-5">
      <div v-for="product in products" :key="product.id">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: 'products'
  })
  useHead({
    title: "Nuxt Dojo Merch"
  })

  // Fetch the products
  const {data: products} = await useFetch("https://fakestoreapi.com/products")
</script>