# SCANDALS 2.0 — Checklist Web App v2 (Synced)

Web checklist mobile-friendly dengan **sinkronisasi tim** — semua anggota tim
melihat progress yang sama secara real-time.

## Cara Deploy ke Vercel

### Opsi A — Upload Langsung (Paling Mudah)
1. Buat akun di https://vercel.com (gratis)
2. Klik **New Project → Browse** dan upload folder `scandals-checklist-v2/`
3. Klik **Deploy**
4. Bagikan URL ke seluruh anggota tim

### Opsi B — Via GitHub
1. Upload folder ini ke repo GitHub
2. Di Vercel → Import Git Repository → pilih repo → Deploy
3. Setiap kali ada update file, Vercel auto-deploy ulang

### Opsi C — Via Vercel CLI
```bash
npm i -g vercel
cd scandals-checklist-v2
vercel --prod
```

## Fitur v2
- ✅ **Progress tersinkron** — semua anggota tim share data yang sama
- 🔄 Tombol Refresh untuk ambil update terbaru dari rekan tim
- 💾 Auto-save 0.6 detik setelah centang (tidak butuh tombol save)
- 📊 Indikator sync: Menyimpan... / Tersimpan HH:MM / Gagal
- 🎨 Tema light, nyaman dibaca di luar ruangan & di HP
- 🔍 Filter: Semua / Foto / Data / Gambar / Teks / Belum
- 🎊 Animasi confetti saat item diselesaikan

## Catatan Teknis
- Storage menggunakan **Claude Artifacts Persistent Storage API**
- Data disimpan sebagai `shared = true` → semua user dapat data yang sama
- Tidak butuh database eksternal, gratis sepenuhnya
- Data tersimpan per artifact/deployment — tidak hilang saat refresh

## Anggota Tim
Cukup bagikan 1 URL Vercel ke semua anggota. Siapapun yang centang,
langsung ter-update untuk semua orang (setelah klik Refresh atau membuka ulang).
