<script setup>

const props = defineProps({
    text: String,
    url: String,
    external: Boolean
})

</script>

<template>
    <a v-if="external" :href="url" target="_blank"
        class="linkbtn block bg-yellow-400 text-green-900 font-bold text-center p-4 rounded-xl shadow-lg">
        {{ text }}
    </a>
    <RouterLink v-else :to="url"
        class="linkbtn block bg-yellow-400 text-green-900 font-bold text-center p-4 rounded-xl shadow-lg">
        {{ text }}
    </RouterLink>
</template>