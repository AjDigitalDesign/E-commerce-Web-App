<template>
    <div class="w-[200px] bg-indigo-700 rounded-l-lg text-white py-4 px-2 transition-all">
        <router-link :to="{name:'app.dashboard'}" class="flex items-center py-3 px-3 transition-colors rounded hover:bg-black/30">
            <span class="mr-2 text-gray-300"><HomeIcon class="w-5"/></span>
            <span class="font-light">
                Dashboard
            </span>
        </router-link>

        <router-link :to="{name:'app.products'}" class="flex items-center py-3 px-3 transition-colors rounded hover:bg-black/30">
            <span class="mr-2 text-gray-300"><BuildingStorefrontIcon class="w-5"/></span>
            <span class="font-light">
                Products
            </span>
        </router-link>

        <router-link :to="{name:'app.dashboard'}" class="flex items-center py-3 px-3 transition-colors rounded hover:bg-black/30">
            <span class="mr-2 text-gray-300"><UserIcon class="w-5"/></span>
            <span class="font-light">
                Users
            </span>
        </router-link>

        <router-link :to="{name:'app.dashboard'}" class="flex items-center py-3 px-3 transition-colors rounded hover:bg-black/30">
            <span class="mr-2 text-gray-300"><ChartBarIcon class="w-5"/></span>
            <span class="font-light">
                Reports
            </span>
        </router-link>
    </div>
</template>

<script setup>
    import { HomeIcon, UserIcon, ChartBarIcon, ViewColumnsIcon, BuildingStorefrontIcon } from '@heroicons/vue/20/solid'



    const {title} = defineProps({
        title: String
    })
</script>

<style scoped>

</style>
