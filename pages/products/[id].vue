<template>
  <div class="min-h-screen max-w-screen-xl mx-auto px-2 lg:px-0 pt-4 pb-20">
    <article>
      <div class="grid md:grid-cols-2 gap-10">
        <div class="md:p-7">
          <img :src="product.image" :alt="product.title" :title="product.title" class="w-full max-w-64 h-auto mx-auto">
        </div>
        <div class="md:p-7">
          <h1 class="text-4xl mb-6">{{ product.title }}</h1>
          <p class="text-xl mb-4">Price - ${{ product.price }}</p>
          <hr>
          <p class="mt-2 text-gray-500">{{ product.description }}</p>
          <div class="block mt-8">
            <NuxtLink class="text-green-500" to="/products">&laquo; Back</NuxtLink>
          </div>
        </div>
      </div>
    </article>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: 'products'
  })
  const route = useRoute()
  const {id} = route.params

  // Fetch the product
  const {data: product, error} = await useFetch(`https://fakestoreapi.com/products/${id}`, {key: id})
  if (!product.value) throw createError({statusCode: 404, statusMessage: "product not found!", fatal: true})

  useHead({
    title: `${product.value.title} | Nuxt Dojo Merch`,
    meta: [
      { name: 'description', content: product.value.description }
    ]
  })
</script>