<script setup>

const props = defineProps({
    text: String,
    url: String,
    disabled: Boolean,
    external: Boolean
})

</script>

<template>
    <div v-if="disabled" class="glass text-center p-4 rounded-xl opacity-50 cursor-not-allowed">
        {{ text }}
    </div>
    <a v-else-if="external" :href="url" target="_blank" class="linkbtn block glass text-center p-4 rounded-xl">
        {{ text }}
    </a>
    <RouterLink v-else :to="url" class="linkbtn block glass text-center p-4 rounded-xl">
        {{ text }}
    </RouterLink>
</template>