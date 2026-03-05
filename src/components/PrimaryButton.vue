<script setup>

const props = defineProps({
    text: String,
    url: String
})

</script>

<template>
    <a :href="url" target="_blank"
        class="linkbtn block bg-yellow-400 text-green-900 font-bold text-center p-4 rounded-xl shadow-lg">
        {{ text }}
    </a>
</template>