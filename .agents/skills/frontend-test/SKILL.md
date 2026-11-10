---
name: frontend-test
description: Select and perform frontend behavior verification for components, API clients and user flows. Use for test work or verifying UI changes; distinguish mock-based evidence from backend integration.
---

# Frontend Test

1. Baca AGENTS.md, docs/TESTING.md dan acceptance criteria pada specs. Inspeksi script/framework yang tersedia; jangan menganggap test runner ada hanya karena dependency UI tersedia.
2. Pilih boundary unit, komponen, client API atau alur BE-FE sesuai risiko. Untuk UI, periksa kondisi relevan termasuk input invalid, error, akses ditolak dan keyboard/fokus. Jangan menambah test yang hanya meniru implementasi.
3. Gunakan fixture tanpa data privat. Mock mengikuti kontrak yang dirujuk dan dilabeli keterbatasannya. Jangan menonaktifkan pengamanan untuk membuat test lulus.
4. Jalankan pemeriksaan yang tersedia; bila framework/dependency belum ada, catat prasyarat dan lanjutkan pemeriksaan independen. Lint/typecheck/build dilaporkan terpisah dari test perilaku. Tidak perlu runtime test untuk perubahan dokumentasi saja.
5. Laporkan boundary, hasil run, skipped/failure dan bukti per acceptance criteria. Perbarui status shared hanya untuk bagian yang terbukti; jangan menyatakan integrasi selesai dari mock.
