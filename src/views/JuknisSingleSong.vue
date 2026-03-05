<script setup>
import Juknis from '../layouts/Juknis.vue'

const accordionData = {
    syarat: {
        label: "Syarat & Ketentuan Umum",
        icon: "📜",
        content: [
            "Lomba berkategorikan solo vokal via online.",
            "Peserta hanya menyanyikan 1 lagu Islami.",
            "Wajib memakai identitas IPNU/IPPNU saat merekam.",
            "Kategori: Vokal Solo IPNU & Vokal Solo IPPNU."
        ]
    },
    teknis: {
        label: "Teknis Pelaksanaan",
        icon: "🎥",
        content: [
            "Durasi video maksimal 5 menit.",
            "Orientasi kamera landscape (Resolusi 720p).",
            "Suara orisinil (Tanpa autotune/audio mixing).",
            "Video diunggah ke Google Drive PC IPNU IPPNU Trenggalek.",
            "Keputusan dewan juri bersifat mutlak."
        ]
    },
    kompetensi: {
        label: "Ketentuan Kompetensi & Pendaftaran",
        icon: "📝",
        content: [
            "Anggota aktif PAC (Dibuktikan dengan softfile SP).",
            "Format file: Nama_Asal PAC_Judul Lagu.",
            "Batas pengiriman: 12 Maret 2026."
        ]
    },
    penilaian: {
        label: "Kriteria Penilaian",
        icon: "📊",
        content: [
            "Materi Vokal (30%): Kualitas & karakter suara.",
            "Teknik Vokal (40%): Intonasi, artikulasi, phasering, diksi.",
            "Ekspresi & Penampilan (30%): Penjiwaan, kostum, & improvisasi."
        ]
    },
    hadiah: {
        label: "Hadiah & Penghargaan",
        icon: "🏆",
        content: [
            "Juara 1, 2, 3: E-Sertifikat + Uang Pembinaan.",
            "Seluruh Peserta: E-Sertifikat Partisipasi."
        ]
    }
}
</script>

<template>
    <div>
        <Juknis :accordion-data="accordionData" title="Lomba Single Song" subtitle="PC IPNU IPPNU Trenggalek 2026" />
    </div>
</template>