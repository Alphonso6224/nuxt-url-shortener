<template>
    <a 
    href="#" 
    class="text-sm mb-5 italic flex items-center gap-2 no-underline"
    @click.prevent="useRouter().back()"
    >
      <Icon name="mdi:arrow-left"/>
      Retour
    </a>
</template>