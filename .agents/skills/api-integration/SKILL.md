---
name: api-integration
description: Connect frontend behavior to the Seller Hub backend API contract, including typed requests, errors and server-state caching. Use for client and API-state changes, not backend endpoint implementation.
---

# API Integration

1. Baca AGENTS.md, docs/API-INTEGRATION.md, docs/SECURITY.md serta spesifikasi fitur di specs. Inspeksi client/cache yang ada dan kontrak backend; catat revisinya, termasuk perubahan lokal yang belum committed.
2. Cocokkan method/path, DTO, response/error, validation, pagination dan authentication. Jika kontrak belum ada/bertentangan, laporkan penghalang; jangan mengarang endpoint atau kebijakan sesi.
3. Implementasikan client/state sesuai arsitektur lokal. Pertimbangkan scope cache, invalidation setelah mutasi, pembatalan request dan duplikasi/retry sesuai kontrak; jangan memakai mock sebagai fallback produksi.
4. Verifikasi boundary sesuai docs/TESTING.md. Fixture contract hanya membuktikan interaksi terhadap fixture; uji terhadap BE nyata diperlukan untuk klaim integrasi.
5. Laporkan kontrak yang digunakan, perubahan, hasil run serta kesenjangan BE/FE. Jika dipanggil frontend-feature, kembali ke pekerjaan yang sama tanpa memulai ulang workflow.
