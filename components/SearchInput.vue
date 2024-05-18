<template>
  <div class="relative">
    <Icon name="mdi:magnify" class="absolute right-[5%] top-[50%] translate-y-[-50%] w-6 h-6"/>
    <input type="text" placeholder="Rechercher un lien"
    class="pl-10 rounded border"
    v-model="modelValue" />
  </div>
</template>

<script lang="ts" setup>

const modelValue = defineModel()

</script>

<style>

</style>