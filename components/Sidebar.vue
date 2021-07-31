<template>
    <nav>
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <NuxtLink
            v-for="({ title, icon, path }, $index) in items"
            :class="{
                'bg-gray-900 text-white': $route.path == path,
                'text-gray-300 hover:bg-gray-700 hover:text-white': $route.path != path,
            }"
            :key="$index"
            :to="path"
            class="
                group
                flex
                items-center
                px-2
                py-2
                text-sm
                font-medium
                rounded-md
            "
        >
            <span :class="{
                'text-gray-300': $route.path == path,
                'text-gray-400 group-hover:text-gray-300': $route.path != path,
            }" v-html="icon"></span>
            <!-- Current: "text-gray-300", Default: "text-gray-400 group-hover:text-gray-300" -->
            {{ title }}
        </NuxtLink>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            items: [{
                icon: '<svg class="text-gray-300 mr-3 h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>',
                title: 'Administrează chiria',
                path: '/',
            },{
                icon: '<svg xmlns="http://www.w3.org/2000/svg" class="text-gray-300 mr-3 h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" /></svg>',
                title: 'Contract curent',
                path: '/sign-contract',
            },{
                icon: '<svg xmlns="http://www.w3.org/2000/svg" class="text-gray-300 mr-3 h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" /></svg>',
                title: 'Tranzacții',
                path: '/insurance',
            },{
                icon: '<svg xmlns="http://www.w3.org/2000/svg" class="text-gray-300 mr-3 h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h2a2 2 0 012 2v6a2 2 0 01-2 2h-2v4l-4-4H9a1.994 1.994 0 01-1.414-.586m0 0L11 14h4a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2v4l.586-.586z" /></svg>',
                title: 'Mesajele mele',
                path: '/messages',
            },{
                icon: '<svg xmlns="http://www.w3.org/2000/svg" class="text-gray-300 mr-3 h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" /></svg>',
                title: 'Servicii',
                path: '/transactions',
            }]
        }
    }
};
</script>

<style>
</style>