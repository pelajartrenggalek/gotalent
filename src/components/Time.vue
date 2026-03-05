<script setup>
import { ref, onMounted, onUnmounted } from "vue"
import { timeline } from "../timeline.js"

const days = ref("00")
const hours = ref("00")
const minutes = ref("00")
const seconds = ref("00")

const targetDate = new Date(timeline.pendaftaran.date).getTime()

let interval = null

const updateCountdown = () => {
    const now = new Date().getTime()
    const distance = targetDate - now

    if (distance <= 0) {
        days.value = "00"
        hours.value = "00"
        minutes.value = "00"
        seconds.value = "00"
        return
    }

    days.value = Math.floor(distance / (1000 * 60 * 60 * 24))
    hours.value = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))
    minutes.value = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
    seconds.value = Math.floor((distance % (1000 * 60)) / 1000)
}

onMounted(() => {
    updateCountdown()
    interval = setInterval(() => {
        updateCountdown()
    }, 1000)
})

onUnmounted(() => {
    clearInterval(interval)
})
</script>

<template>
    <div class="glass rounded-2xl p-5 mb-8 text-center">
        <h2 class="font-semibold mb-3">
            ⏳ Batas Pendaftaran
        </h2>
        <div class="grid grid-cols-4 gap-3 text-center">
            <div class="glass rounded-lg p-2">
                <div id="days" class="text-2xl font-bold">{{ days }}</div>
                <div class="text-xs">Hari</div>
            </div>
            <div class="glass rounded-lg p-2">
                <div id="hours" class="text-2xl font-bold">{{ hours }}</div>
                <div class="text-xs">Jam</div>
            </div>
            <div class="glass rounded-lg p-2">
                <div id="minutes" class="text-2xl font-bold">{{ minutes }}</div>
                <div class="text-xs">Menit</div>
            </div>
            <div class="glass rounded-lg p-2">
                <div id="seconds" class="text-2xl font-bold">{{ seconds }}</div>
                <div class="text-xs">Detik</div>
            </div>
        </div>
    </div>
</template>