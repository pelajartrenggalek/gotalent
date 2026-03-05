<script setup>
</script>

<template>
    <div class="bg"></div>
    <div class="text-white flex justify-center min-h-screen">
        <div class="max-w-2xl w-full p-5">

            <RouterLink to="/" class="block w-full mb-5 border border-white/30 rounded-2xl overflow-hidden">
                <img src="./header.jpg" alt="Cover" class="w-full">
                <p class="text-center text-xl font-bold text-shadow-lg pt-5 py-6 px-3 bg-white/10 backdrop-blur-sm">
                    Dalam Rangka Harlah IPNU 72 - IPPNU 71
                </p>
            </RouterLink>

            <RouterView />

            <div class="text-center text-xs opacity-60 mt-6">
                2026 &copy; Ekosistem Digital Organisasi
            </div>

        </div>
    </div>
</template>

<style>
body {
    font-family: 'Poppins', sans-serif;
    background: url('./bg.webp') center center/cover no-repeat;
}

.bg {
    opacity: .85;
    background: linear-gradient(-45deg, #06344e, #06255f, #06162c, #060c2c);
    background-size: 400% 400%;
    animation: gradient 10s ease infinite;
    width: 100vw;
    height: 100vh;
    position: fixed;
    z-index: -1;
}

@keyframes gradient {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

.glass {
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.linkbtn {
    transition: all .25s;
}

.linkbtn:hover {
    transform: scale(1.05);
}
</style>