<template>
    <div class="flex min-h-full bg-gray-200">
        <!-- Sidebar -->
        <SideBar :class="{'-ml-[200px]' : !sidebarOpened}"/>

        <!-- Main -->
        <div class="flex-1">
            <Navbar @toggle-sidebar="toggleSidebar" />

            <!-- Content-->
            <main class="p-6">
                <!-- Content -->
                <div class="p-4 rounded bg-white">
                   <router-view></router-view>
                </div>
            </main>
        </div>
    </div>
</template>

<script setup>
import {ref, onMounted, onUnmounted} from "vue";

import SideBar from "./SideBar.vue";
    import TopHeader from "./Navbar.vue";
import Navbar from "./Navbar.vue";

    const {title} = defineProps({
        title: String
    })

    const sidebarOpened = ref(true)

    function toggleSidebar() {
        sidebarOpened.value = !sidebarOpened.value
    }

    onMounted( () => {
        handleSidebarOpened()
        window.addEventListener('resize', handleSidebarOpened)
    })

    onUnmounted( () => {
        window.addEventListener('resize', handleSidebarOpened)
    })

    function handleSidebarOpened() {
        sidebarOpened.value = window.outerWidth > 768;
    }
</script>

<style scoped>

</style>
