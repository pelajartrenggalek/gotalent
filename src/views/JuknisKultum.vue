<script setup>
import Juknis from '../layouts/Juknis.vue'

const accordionData = {
    umum: {
        label: "Ketentuan Umum",
        icon: "📜",
        content: [
            "Lomba Kultum Ramadhan diselenggarakan oleh PC IPNU-IPPNU dalam rangka memperingati Harlah IPNU-IPPNU.",
            "Peserta adalah kader IPNU-IPPNU tingkat PAC/PK se-cabang.",
            "Setiap PAC/PK mengirimkan maksimal 2 peserta (1 IPNU & 1 IPPNU).",
            "Peserta wajib berpakaian rapi, sopan, dan sesuai atribut organisasi.",
            "Keputusan dewan juri bersifat mutlak dan tidak dapat diganggu gugat."
        ]
    },
    tema: {
        label: "Tema Kultum",
        icon: "🕌",
        content: [
            "Spirit Fastabiqul Khairat di Bulan Ramadhan.",
            "Peran Pelajar NU dalam Syiar Agama.",
            "Tema lain dapat dikembangkan oleh peserta selama masih relevan dengan nilai Ramadhan dan dakwah pelajar NU."
        ]
    },
    teknis: {
        label: "Ketentuan Teknis",
        icon: "🎤",
        content: [
            "Durasi kultum 7–10 menit.",
            "Peserta dilarang membaca teks secara penuh (boleh membawa poin-poin).",
            "Menggunakan bahasa Indonesia yang baik dan santun (boleh diselingi dalil Arab).",
            "Materi wajib mencantumkan minimal 1 ayat Al-Qur’an dan 1 hadits.",
            "Tidak diperkenankan mengandung unsur SARA, politik praktis, dan ujaran kebencian."
        ]
    },
    penilaian: {
        label: "Kriteria Penilaian",
        icon: "📊",
        content: [
            "Kesesuaian Tema (20%).",
            "Penguasaan Materi (25%).",
            "Retorika & Artikulasi (20%).",
            "Dalil & Kedalaman Isi (15%).",
            "Adab & Penampilan (10%).",
            "Kepercayaan Diri (10%)."
        ]
    },
    pelaksanaan: {
        label: "Teknis Pelaksanaan",
        icon: "🎥",
        content: [
            "Pelaksanaan lomba tanggal 1–14 Maret 2026 secara online.",
            "Waktu bersifat tentatif.",
            "Tempat pengambilan video di Masjid/Mushola atau tempat umum yang menarik di daerah masing-masing.",
            "Pengumpulan video melalui Google Drive (setiap kategori dibuatkan folder sendiri).",
            "Sistem lomba langsung tanpa babak kualifikasi."
        ]
    }
}
</script>

<template>
    <div>
        <Juknis :accordion-data="accordionData" title="Lomba Kultum Ramadhan"
            subtitle="PC IPNU IPPNU Trenggalek 2026" />
    </div>
</template>