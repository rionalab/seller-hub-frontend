# Frontend Coding Standards

Ikuti TypeScript strictness pada tsconfig dan format/lint yang tersedia pada proyek. Nama file komponen mengikuti tipe PascalCase; hooks memakai use prefix; fungsi/variabel camelCase. Gunakan nama lengkap yang menunjukkan feature dan tujuan, hindari file generik yang sulit dibedakan. Ikuti pola kode yang sudah disepakati tanpa refactor tak terkait.

Pisahkan komponen tampilan, akses API dan logika yang perlu diuji sesuai tanggung jawab. Type request/response mengikuti kontrak; jangan gunakan any untuk menyembunyikan ketidaksesuaian. Jangan menggandakan state server atau aturan bisnis tanpa kebutuhan.

Setiap alur UI mempertimbangkan loading, empty, error, success dan akses ditolak sesuai fitur. Form validation memberi bantuan pengguna; validasi server tetap otoritatif. Utamakan elemen semantik, label, keyboard dan fokus yang sesuai. Pesan tidak membocorkan data privat atau stack trace.

Keamanan mengikuti SECURITY.md, integrasi mengikuti API-INTEGRATION.md, dan bukti test mengikuti TESTING.md. Jangan mengubah expected test/kontrak hanya agar pemeriksaan lulus.
