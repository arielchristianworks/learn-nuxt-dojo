<template>
  <div>
    <header class="bg-white shadow">
      <nav class="flex flex-row gap-4 items-center max-w-screen-xl mx-auto px-2 lg:px-0 py-4">
        <h1 class="logo"><NuxtLink to="/">Nuxt Dojo Merch</NuxtLink></h1>
      </nav>
    </header>

    <div>
      <slot />
    </div>

    <footer class="bg-green-100 min-h-40">
      <div class="max-w-screen-xl mx-auto px-2 lg:px-0 py-8">
        <h1 class="logo pl-2 mb-4"><NuxtLink to="/">Nuxt Dojo Merch</NuxtLink></h1>
        <ul class="flex flex-col">
          <li><NuxtLink class="nav-link" to="/">Home</NuxtLink></li>
          <li><NuxtLink class="nav-link" to="/about">About</NuxtLink></li>
          <li><NuxtLink class="nav-link" to="/products">Products</NuxtLink></li>
        </ul>
      </div>
    </footer>
  </div>
</template>