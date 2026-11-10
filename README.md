# Seller Hub Frontend

Frontend Seller Hub dengan React, TypeScript dan Vite. Package saat ini juga memuat Ant Design, React Router, TanStack Query dan dayjs. Entry aktif masih template Vite; folder fondasi yang tersedia belum membuktikan fitur bisnis selesai.

Baca [AGENTS](AGENTS.md), [Architecture](docs/ARCHITECTURE.md), [Setup](docs/SETUP.md) dan [TODO](docs/TODO.md). Kebutuhan bisnis bersumber dari [seller-hub-specs](../seller-hub-specs/README.md), kontrak API dari backend. Ketiga repository di-checkout sebagai folder sejajar.

Script proyek: pnpm dev, pnpm build, pnpm check. Framework test perilaku belum ditentukan; lint/typecheck bukan bukti integrasi. Jangan menaruh secrets pada environment yang dibundel ke browser.
