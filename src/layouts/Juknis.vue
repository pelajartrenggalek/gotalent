<script setup>
import { ref } from 'vue'

const activeKey = ref('syarat')

const toggle = (key) => {
    activeKey.value = activeKey.value === key ? null : key
}

const props = defineProps({
    title: String,
    subtitle: String,
    accordionData: Object
})

</script>

<template>
    <div class="glass p-6 flex flex-col items-center rounded-2xl">

        <div class="text-center mb-10">
            <h1 class="text-3xl font-bold text-white mb-2 tracking-tight">{{ title }}</h1>
            <p class="text-emerald-300 font-medium">{{ subtitle }}</p>
        </div>

        <div class="w-full max-w-2xl space-y-4">
            <div v-for="(item, key) in accordionData" :key="key"
                class="glass border border-white/15 rounded-2xl overflow-hidden transition-all duration-500"
                :class="activeKey === key ? 'bg-white/10' : 'bg-white/5 hover:bg-white/10'">
                <button @click="toggle(key)"
                    class="w-full flex items-center justify-between p-5 cursor-pointer text-left">
                    <span class="flex items-center gap-4">
                        <span class="p-2 bg-emerald-500/20 rounded-lg shrink-0">{{ item.icon }}</span>
                        <span class="font-semibold text-white tracking-wide">{{ item.label }}</span>
                    </span>

                    <svg xmlns="http://www.w3.org/2000/svg"
                        class="h-5 w-5 transition-transform duration-500 text-emerald-400"
                        :class="activeKey === key ? 'rotate-180' : 'rotate-0'" fill="none" viewBox="0 0 24 24"
                        stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                    </svg>
                </button>

                <div class="grid transition-[grid-template-rows] duration-500 ease-in-out"
                    :class="activeKey === key ? 'grid-rows-[1fr] opacity-100' : 'grid-rows-[0fr] opacity-0'">
                    <div class="overflow-hidden">
                        <div class="px-6 pb-6 pt-2 border-t border-white/5">
                            <ul class="space-y-3 pt-4">
                                <li v-for="(line, index) in item.content" :key="index"
                                    class="flex items-start gap-3 text-sm text-slate-200">
                                    <span
                                        class="h-1.5 w-1.5 bg-emerald-400 rounded-full mt-1.5 shrink-0 shadow-[0_0_5px_rgba(52,211,153,0.8)]"></span>
                                    {{ line }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>