# Seller Hub Frontend AI Instructions

## Mulai bekerja dan sumber utama

Baca ../seller-hub-specs/AGENTS.md, ../seller-hub-specs/docs/PRODUCT.md, FEATURE-STATUS.md serta spesifikasi fitur terkait di docs/features/ milik specs. Path saudara dihitung dari root repository. Baca docs/ARCHITECTURE.md dan docs/CODING-STANDARDS.md lokal sebelum desain/implementasi. Jika specs tidak tersedia, laporkan prasyarat checkout dan lanjutkan pekerjaan independen; jangan membuat aturan bisnis atau salinan PRODUCT lokal.

Kebutuhan, prioritas, business rules dan acceptance criteria dimiliki specs. Struktur kode, keamanan browser dan test FE dimiliki docs/ lokal. Kontrak API aktif berasal dari ../seller-hub-backend/docs/API-CONTRACT.md dan openapi.json, bukan mock atau asumsi UI. Baca docs/API-INTEGRATION.md sebelum integrasi. Jika kontrak bertentangan dengan spesifikasi, angkat keputusan sebelum mengimplementasikan bagian yang bergantung padanya.

Ikuti ../seller-hub-specs/docs/FEATURE-WORKFLOW.md sebagai partner kritis dengan perspektif Senior Business Analyst, Product Owner dan Principal Software Architect. Pisahkan fakta, asumsi, rekomendasi dan keputusan. Tanyakan hanya keputusan yang diperlukan melalui pilihan interaktif bila tersedia; jangan mengulang keputusan yang sudah disetujui atau memperluas scope otomatis.

## Routing

- Analisis/desain/implementasi fitur UI: .agents/frontend.md dan .agents/skills/frontend-feature/SKILL.md.
- Integrasi API dan state server: docs/API-INTEGRATION.md dan .agents/skills/api-integration/SKILL.md.
- Pengujian: .agents/testing.md dan docs/TESTING.md; gunakan .agents/skills/frontend-test/SKILL.md untuk verifikasi perilaku yang diperlukan.
- Keamanan browser/sesi/data: .agents/security.md dan docs/SECURITY.md; cocokkan bagian perubahan yang relevan pada tiap implementasi.
- Setup/CI: docs/SETUP.md. Status teknis aktual: docs/TODO.md.

frontend-feature menjadi alur utama; spesialis hanya untuk bagian terdampak. Jangan memulai ulang workflow dari spesialis. File peran bukan subagent otomatis. Dokumen standar menjadi sumber aturan; skill berisi langkah kerja dan peran berisi fokus pemeriksaan.

## Cara bekerja

Inspeksi kode, package.json, lockfile dan perubahan lokal sebelum mengedit. Pertahankan file pengguna; adanya scaffold kosong tidak berarti fitur tersedia. Gunakan stack proyek yang tercatat, tanpa memasang framework atau mengganti arsitektur diam-diam. Jangan menyalin pola .NET ke frontend.

UI bukan batas authorization; jangan membuat login palsu, token demo atau menganggap hidden button sebagai pengamanan. Jangan membaca/menampilkan secrets atau mengirim data privat ke log. Konfigurasi browser bukan tempat secrets.

Lakukan pekerjaan yang diotorisasi, verifikasi sesuai dampak, dan laporkan lulus/gagal/belum diuji. Update TODO teknis lokal serta status BE/FE/integrasi di specs sesuai bukti. Catat revisi specs dan kontrak; mock tidak membuktikan integrasi. Tidak commit/push, deploy atau mengubah backend tanpa cakupan yang mengotorisasinya.
