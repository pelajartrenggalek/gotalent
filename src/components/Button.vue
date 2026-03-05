<script setup>

const props = defineProps({
    text: String,
    url: String,
    disabled: Boolean
})

</script>

<template>
    <a v-if="!disabled" :href="url" target="_blank" class="linkbtn block glass text-center p-4 rounded-xl">
        {{ text }}
    </a>
    <div v-else class="glass text-center p-4 rounded-xl opacity-50 cursor-not-allowed">
        {{ text }}
    </div>
</template>