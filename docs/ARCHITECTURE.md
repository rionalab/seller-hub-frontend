# Frontend Architecture

## Kondisi checkout

package.json menetapkan React, TypeScript, Vite, Ant Design, React Router, TanStack Query dan dayjs. pnpm-lock.yaml tersedia. Ikuti versi project/lockfile; keberadaan dependency tidak membuktikan sudah diintegrasikan. Tidak memilih stack baru pada pekerjaan dokumentasi ini.

Entry aktif src/main.tsx masih memuat src/App.tsx (template Vite). File src/app/App.tsx, router, providers, query-client, layouts dan shared yang ditemukan masih kosong saat inspeksi. Jangan menganggap ada routing, autentikasi atau integrasi API yang sudah berjalan. Jangan menimpa file tersebut tanpa membaca keadaan terbaru.

## Batas tanggung jawab

- src/app/: composition aplikasi, provider dan router saat diimplementasikan.
- src/layouts/: shell halaman yang benar-benar digunakan; nama Admin/Seller bukan keputusan scope produk.
- src/shared/: komponen, konfigurasi, API client dan utilitas yang digunakan lintas fitur; jangan menaruh aturan bisnis feature di sini.
- src/theme/ dan src/styles/: theme/styles bersama.
- Kode fitur ditempatkan dekat perilaku yang dimilikinya; pilih detail folder feature ketika fitur pertama ditentukan, mengikuti prinsip kepemilikan starter tanpa membuat folder kosong.

Server-state mengikuti kontrak backend; state interaksi lokal tetap dekat komponen. Pilihan persistence sesi, route guard dan permission model belum ditetapkan. UI membantu pengguna, sementara BE menegakkan otorisasi dan invariant bisnis. Komponen reusable dibuat berdasarkan kebutuhan nyata.

Dokumen bisnis bersumber dari specs; kontrak HTTP bersumber dari backend. Jangan membuat domain Product/Order hanya untuk melengkapi scaffold.
