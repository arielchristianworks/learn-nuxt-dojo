<template>
  <div>
    <header class="bg-white shadow">
      <nav class="flex flex-row gap-4 items-center max-w-screen-xl mx-auto px-2 lg:px-0 py-4">
        <h1 class="logo"><NuxtLink to="/">Nuxt Dojo</NuxtLink></h1>
        <ul class="flex flex-row gap-2 items-center">
          <li><NuxtLink class="nav-link" to="/">Home</NuxtLink></li>
          <li><NuxtLink class="nav-link" to="/about">About</NuxtLink></li>
          <li><NuxtLink class="nav-link" to="/products">Products</NuxtLink></li>
        </ul>
      </nav>
    </header>

    <div>
      <slot />
    </div>
  </div>
</template>