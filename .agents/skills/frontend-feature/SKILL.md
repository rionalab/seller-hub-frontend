---
name: frontend-feature
description: Analyze, design and implement Seller Hub frontend features using the project's React and TypeScript stack. Use for user flows, screens, forms or changes spanning UI and API state.
---

# Frontend Feature

1. Baca AGENTS.md lokal, ../seller-hub-specs/docs/FEATURE-WORKFLOW.md dan spesifikasi fitur terkait (path dari root repo), lalu architecture/coding standards lokal. Inspeksi entry point dan perubahan pengguna; jangan menganggap scaffold sudah berjalan.
2. Identifikasi aktor, tujuan, alur, akses, acceptance criteria serta fakta/asumsi/keputusan terbuka. Periksa loading, empty, error, success, validasi, keyboard/fokus dan kebutuhan yang terlewat sesuai dampak. Ajukan rekomendasi/tradeoff; tanyakan penghalang keputusan tanpa memperluas scope.
3. Cocokkan kontrak backend dengan perilaku UI. Gunakan api-integration hanya bila koneksi/state API terdampak; jangan memulai ulang workflow feature. Endpoint yang belum ada ditandai dependency, bukan ditebak dari desain.
4. Implementasikan perubahan yang diotorisasi mengikuti struktur/paket saat ini. Periksa SECURITY.md sesuai bagian yang berubah. Jangan membuat izin bisnis atau token/login palsu; hidden UI bukan authorization.
5. Pilih verifikasi melalui .agents/testing.md dan docs/TESTING.md; gunakan frontend-test untuk boundary yang diperlukan. Jangan memasang framework hanya untuk mengikuti checklist.
6. Update spesifikasi yang berubah di specs dengan keputusan yang disetujui, status BE/FE/integrasi dan bukti lokal. Laporkan perubahan, hasil, dependency dan batas mock. Untuk tugas desain saja, serahkan rancangan/keputusan terbuka tanpa mengubah runtime.
