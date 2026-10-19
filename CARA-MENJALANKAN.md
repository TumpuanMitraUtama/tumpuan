# Cara Menjalankan Website PT Tumpuan Mitra Utama

Website ini memakai React + TanStack Start. Untuk menjalankannya, komputer perlu punya
**Node.js versi 20 atau lebih baru** (unduh gratis di https://nodejs.org).

## 1. Buka di komputer sendiri (mode pengembangan)

1. Buka folder `pt-tumpuan-mitra-utama` di Terminal (macOS) atau Command Prompt (Windows).
2. Ketik perintah berikut, satu per satu, lalu tekan Enter:

```
npm install
npm run dev
```

3. Setelah muncul alamat seperti `http://localhost:8080`, buka alamat itu di browser.
4. Untuk menghentikannya, tekan `Ctrl + C` di jendela terminal.

## 2. Membuat versi siap online (build)

```
npm run build
```

Hasilnya ada di folder `dist`. Folder ini yang diunggah ke layanan hosting
(netlify, vercel, cloudflare pages, atau hosting lain yang mendukung aplikasi React).

Untuk melihat hasil build di komputer sendiri:

```
npm run preview
```

## 3. Mengganti teks, nomor telepon, dan alamat

- Semua teks bahasa Indonesia dan Inggris: `src/lib/i18n.tsx`
- Nomor WhatsApp, email, dan alamat: bagian atas `src/routes/index.tsx`
  (baris `const WA = ...`, `const EMAIL = ...`, dan alamat di bagian kontak/footer)
- Logo dan foto: folder `src/assets` — ganti filenya dengan nama yang sama,
  atau ganti nama file di dalam kode.

## 4. Ganti bahasa

Tombol **ID / EN** di kanan atas halaman akan langsung mengganti seluruh teks.
Bahasa pilihan pengunjung tersimpan di browser mereka.

## 5. Kalau ada masalah

- `npm install` gagal: pastikan Node.js sudah terpasang (`node -v` harus menampilkan angka).
- Halaman kosong: hapus folder `node_modules` lalu ulangi `npm install`.
