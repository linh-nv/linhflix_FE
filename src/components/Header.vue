<template>
    <nav class="z-[999999] fixed justify-between border-b border-b-slate-600 bg-slate-950 backdrop-blur-[5px] w-full h-16 flex items-center px-8 transition duration-300 py-3">
        <div class="menu lg:hidden" @click="toggleDrawer">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 5.25h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5" />
            </svg>
        </div>
        <a-drawer
            class="border-r border-r-slate-600 pt-16 lg:hidden"
            :placement="placement"
            :closable="false"
            style="background-color: #020617;"
            :open="open"
            @close="onClose"
        >
            <p>Some contents...</p>
            <p>Some contents...</p>
            <p>Some contents...</p>
        </a-drawer>
        <span class="text-red-500 uppercase font-black">LinhPhim</span>
        <span>Admin</span>
    </nav>
</template>
<script setup>
import { ref } from 'vue';
const placement = ref('left');
const open = ref(false);
const toggleDrawer = () => {
    open.value = !open.value; // Đảo ngược trạng thái của a-drawer
};
const onClose = () => {
    open.value = false;
};
</script>
