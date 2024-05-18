<template>
    <div class="">
        <GoBack />
        <nav class="prose flex justify-between items-center mb-4 min-w-full">
            <h1 class="mb-0">Mes liens</h1>
            <div class="flex justify-between items-center gap-5">
                <SearchInput :model-value="search" />
                <NuxtLink to="/links/create"
                    class="no-underline px-4 py-2 text-white bg-gray-600 hover:bg-gray-800 rounded-md transiton duration-300">
                    Créer un lien
                </NuxtLink>
            </div>
        </nav>
        <table class="w-full border text-sm text-left text-gray-500">
            <thead class="text-xs text-gray-700 uppercase bg-gray-50">
                <tr>
                    <th>Lien Complet</th>
                    <th>Lien court</th>
                    <th>Nbr.Vues</th>
                    <th>Actions</th>
                    <th aria-label="Rafraîchir">
                        <Icon class="h-6 w-6" name="mdi:refresh" />
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="link in links" :key="link.id" class="bg-white border-b text-left">
                    <td>
                        <a :href="link.full_links" target="_blank">
                            {{ link.full_links }}
                        </a>
                    </td>
                    <td>
                        <a href="`${useRuntimeConfig().public.appUrl}/${link.short_links}`" target="_blank">
                            {{ `${useRuntimeConfig().public.appUrl.replace(/^http(s?):\/\//, "")}/${link.short_links}`
                            }}
                        </a>
                    </td>
                    <td>
                        {{ link.views }}
                    </td>
                    <td class="flex flex-nowrap gap-2">
                        <button>
                            <Icon class="h-6 w-6 text-red-500" name="mdi:trash" />
                        </button>
                        <NuxtLink :to="`/links/${link.id}`">
                            <Icon class="h-6 w-6 text-blue-500" name="mdi:pencil" />
                        </NuxtLink>
                    </td>
                    <td></td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script lang="ts" setup>
const links = [
    {
        short_links: "lkj24df",
        full_links: "https://youtube.com",
        views: 1,
        id: 'b11e181e-2865-400a-9707-356aa81ca273',
    },
    {
        short_links: "lkj24df",
        full_links: "https://w3school.com",
        views: 3,
        id: 'dde8229f-735a-44dc-976a-f0538c2dbfdf',
    },
    {
        short_links: "lkj24df",
        full_links: "https://devdocs.com",
        views: 10,
        id: 'c88d1767-6e87-4c73-845e-d45f6e0358d0',
    },
    {
        short_links: "lkj24df",
        full_links: "https://perplexity.com",
        views: 7,
        id: '30c922ac-bdd1-49e1-9733-fe516490a844',
    },
];

let search = ref<string>("");
</script>

<style>
th {
    @apply px-6 py-3
}

td {
    @apply px-6 py-3
}
</style>
