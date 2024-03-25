<template>
    <Header/>
    <div class="box flex">
        <div class="sider-bar bg-slate-950 border-r border-r-slate-600 w-1/3 max-w-[300px] h-screen lg:block hidden px-8 pt-20">
            SIDER BAR
        </div>
        <div class="w-full px-8 pt-20">
            <div class="container">
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>
<script>
import Header from '../components/Header.vue';

export default {
    components: {
        Header
    }
}
</script>