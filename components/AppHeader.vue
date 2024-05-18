<template>
  <header>
    <nav class="flex items-center justify-between bg-gray-800 text-white p-4 shadow-sm shadow-gray-900 mb-5 sticky top-0">
      <NuxtLink to="/" class="cursor-pointer text-3xl font-bold">
        URLShortify
      </NuxtLink>

      <div class="space-x-3">
        <NuxtLink to="/me" class="cursor-pointer">
          Profile
        </NuxtLink>

        <NuxtLink to="/links" class="cursor-pointer">
          Liens
        </NuxtLink>

        <NuxtLink to="#" class="cursor-pointer">
          <Icon name="mdi:logout" />
        </NuxtLink>
      </div>
    </nav>
  </header>
</template>
