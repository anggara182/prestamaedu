# Prestama Education: konten Instagram

Les privat SD & SMP. Tentor datang ke rumah, atau online. Value utama: metode menyesuaikan gaya belajar tiap anak.
Tagline: **Langkah Pasti Menuju Prestasi**. Peran Claude di repo ini: content strategist, copywriter, graphic designer.

## Brand (sudah disetujui)

- Palet dari logo: oranye `#F39A1E`, biru `#1F7FC4`, biru gelap `#0F4E86`, cream `#FBF8F3`, ink `#1D1D1F`.
- Wordmark: PRESTAMA (oranye) di atas EDUCATION (biru), Montserrat 800. Di latar oranye/biru: wordmark dan logo **putih semua**.
- Tipografi: judul Inter Tight 700 rapat (gaya Apple), kata kunci DM Serif Display italic. Teks isi Inter/Inter Tight.
- Kesan: clean, profesional, elegan, well-educated. Hindari props ramai.

## Value pilar (post 03 "Mengapa Prestama")

1. **Privat & personal**: satu tentor fokus pada satu murid, metode sesuai gaya belajarnya.
2. **Tentor berpengalaman**: terbiasa mendampingi beragam karakter murid.
3. **Datang ke rumah**: Kota Jogja dan sekitarnya.
4. **Online dari mana saja**: untuk yang di luar Jogja.

Setiap kali menyebut area layanan Jogja, sebutkan juga opsi online untuk yang di luar Jogja.

## Nada konten

- Selalu positif dan memberdayakan. **Jangan pernah** terkesan mengejek, menyindir, atau menyalahkan orang tua maupun anak
  (tidak ada format "jangan bilang X", tidak ada kalimat merendahkan yang dicoret). Tawarkan hal yang bisa langsung dipraktikkan.

## Karakter

- Rig flat SVG di `char/` (diadaptasi dari cast-bank repo wni), 100% kode, tanpa gambar AI.
- Murid SD (putih-merah, dasi), SMP (putih-biru, celana panjang), kakak tentor berhijab.
- **Karakter berhijab wajib menutup aurat:** kerudung menutup leher sampai dada, lengan panjang, rok panjang, kaki bersepatu.
- Framing bervariasi (close-up, medium, full) dan pose sesuai konteks. Skala konsisten; medium shot menempel ke tepi bawah frame.
- Teks tidak boleh menutupi wajah.
- **Stok karakter (20):** `char/cast.tsx` (tentor, murid SD/SMP seragam/Pramuka/baju rumah, orang tua). `render-cast.tsx` menghasilkan 6 pose × med/full
  ke `char/out-cast/` dan lembar per grup (kanvas page "Karakter"). Set/properti adegan bersama di `char/sets.tsx`.
- **Reels tidak ditampilkan di grid utama** (matikan "tampilkan di grid profil" saat posting). Cover Reels khusus, **warna per pilar**:
  Tips Ngajar = oranye, Bahas Soal = biru, Trik Kilat = putih/cream. File: `output/cover-reels/` (1080×1920, judul besar + karakter).
- **Warna grid selang-seling** (disetujui): dua post berturut-turut tidak boleh sewarna (oranye/cream/biru), dan tiap post
  beda warna dengan post 3 sebelumnya (yang tepat di atasnya di grid). Cover Reels diatur warnanya untuk menjaga pola.
- **Komposisi feed** (dari referensi adrian): karakter/adegan jadi pusat frame (40–60%), judul pendek dan besar, satu properti yang bercerita,
  bingkai brand konsisten (logo atas, tagline/kontak bawah).
- Adegan still real-life (kamar belajar, teras rumah) untuk post feed: `char/render-scenes-w1.tsx` → `assets/char/scene-*.svg`. Dipakai sebagai tile bersudut bulat (radius 36) di bawah judul. Siku duduk di meja pakai `elbows` manual supaya tidak mekar ke samping.

## Reels 3× seminggu

Senin **Tips Ngajar di Rumah**, Kamis **Bahas Soal**, Sabtu **Trik Kilat**. Detail di `PILAR-REELS.md`; komponen bersama `video/src/kit.tsx`;
VO lewat `video/vo/make_vo.py`.

## Template video BAHAS SOAL (Reels + Story) — final, ikuti persis

Referensi: `video/src/BahasSoal01.tsx`, output `output/video/bahas-soal-01.mp4`, detail di `PILAR-BAHAS-SOAL.md`.

1. **Hook** (latar oranye, tanpa subtitle): **jangan kaitkan dengan pilihan A–D.** Pakai mitos/anggapan umum yang dibantah, mis. "Gagasan utama pasti ada di kalimat pertama. Yakin? Belum tentu!" Kata kunci mitos dicoret + cap (BELUM TENTU!/SALAH). Karakter murid boleh.
2. **Soal** (latar terang): kartu soal di atas, pilihan A–D tepat di bawah kartu.
   **Soal cerita:** saat soal dibacakan, tampilkan **adegan cerita beranimasi** sesuai konteks (tokoh bergerak, benda
   muncul/berpindah mengikuti kata VO, chip angka besar). Komponen `video/src/story.tsx` (rig hidup dari `video/src/rig/`,
   salinan `char/Figure.tsx`, `cast.tsx`, `sets.tsx`; kalau rig di `char/` diubah, salin ulang). Panel di atas kartu soal.
3. **Cara 1 · Lihat polanya/gambarnya**: **pakai ilustrasi atau adegan, jangan terasa textbook.** Mis. panel komik per kalimat soal (Dika menyiram, memupuk, …) atau diagram benda nyata. Tanpa karakter "presenter", tanpa keterangan "untuk anak visual". Karakter di dalam ilustrasi cerita boleh.
4. **Cara 2 · Coba langsung**: VO langsung "Cara kedua. …" (tanpa kalimat pengantar). Benda nyata/aktivitas (mis. gelas takar, memberi judul = sampul buku cerita). Hasil di tengah.
   **Penjelasan tetap komprehensif:** sebutkan konsep/istilahnya (mis. rincian vs kesimpulan, paragraf induktif vs deduktif) dengan visual pendukung (diagram sederhana).
5. **Jawaban**: angka hasil besar, pilihan A–D muncul lalu jawaban menyala + confetti, lalu kartu "Trik cepat".
6. **CTA** (latar oranye, tanpa subtitle, elemen minimal, di tengah): "Jawabanmu tadi bener nggak?" (**jangan pakai "hayo"**, pelafalan TTS-nya aneh) → tombol Follow ditekan jadi Following → "biar nggak ketinggalan materi lain". Tentor + murid di bawah, muncul sejak awal CTA. **Tanpa** pill layanan, logo besar, atau slogan.

Aturan teknis:
- 1080×1920, 30 fps, ±55–60 detik, −14 LUFS. Area aman gabungan Reels & Story: konten penting di y 260–1580, sisi kanan bawah bebas untuk ikon Reels. Tidak ada progress bar buatan.
- Header tetap: pill `BAHAS SOAL #N` kiri + wordmark kanan, di y ±270.
- **Subtitle hanya di bagian pembahasan (latar terang)**: gaya Apple (kata muncul dari blur), bold biru gelap `#0F4E86`, tanpa kotak, maks 4 kata per baris, di y ±1495.
- Semua animasi dikunci ke timing kata VO.
- Latar terang: cream polos dengan gradasi halus, tanpa lingkaran dekoratif.
- VO: ai33, suara **Siti** (`elevenlabs_WAotVoK2Yv2ufjocfYYs`), speed 1.05, seluruh naskah satu take. Timing kata via ElevenLabs forced alignment.
  Patuhi antrean ai33 bersama: cek task pending (`/v3/tasks`) sebelum submit, jarak submit ≥15 detik.
- Musik: instrumental ceria, di-duck otomatis di bawah VO. SFX ringan (pop, whoosh, ding).

## Konten feed

- 9 post aktivasi di kanvas Design (page "Post Aktivasi"), sumber di `canvas/` dan `src/build.mjs`.
- Caption di `CAPTIONS.md`. WhatsApp konsultasi & pendaftaran: **0857-2926-9143** (link: wa.me/6285729269143). Area layanan: **Kota Jogja dan sekitarnya** untuk les ke rumah; di luar Jogja lewat les online. Hashtag kota `#LesPrivatJogja`. Data lain yang belum ada tetap placeholder `[...]`, jangan dikarang.
- Klaim/tanggal (mis. jadwal TKA) harus bersumber; tandai bila belum resmi.

## Repliz (penjadwalan)

- Kunci `REPLIZ_ACCESS_KEY`/`REPLIZ_SECRET_KEY` di environment membuka workspace yang juga berisi akun WNI dan akun horor.
  **Jangan pernah menyentuh akun selain Prestama.** Akun Prestama belum ditautkan (cek 17 Nov 2026).
- Sebelum menjadwalkan apa pun, kirim usulan jadwal (tanggal, jam, akun) dan tunggu persetujuan.

## Arah desain v2 (disetujui 18 Nov 2026, page "Post Aktivasi v2")

- Gaya Apple: latar set ilustrasi di-blur (depth of field) dengan karakter tajam di depan, gradient lembut, tipografi Inter Tight,
  teks pendukung abu-abu, tanpa bentuk miring/kapsul/neo-brutalist. Sebagian post full-bleed tanpa frame. Feather pakai progressive blur
  (`pblur` di `src/aktivasi_v3.py`), karakter tidak pernah dibuat transparan.
- Biru aksen di atas oranye: gradient `#1E78CC → #1259A6` (bukan navy `#0F4E86`).
- Logo di latar terang: `assets/logo-blue-orange.png` (lampu oranye, buku biru). Latar oranye/biru: logo putih.
- Spasi headline (revisi 18 Nov, user: "rengkat banget dan kepanjangan"): `.T` = letter-spacing 0, line-height 1.05.
  Judul kecil maks −0.015em, angka besar maks −0.015em. Jarak headline → sub-teks minimal ±28 px.
  Headline maksimal 2–3 baris pendek; kalimat panjang dipecah jadi headline singkat + sub-teks abu-abu.
- Kanvas sering diedit langsung oleh user: selalu baca file live sebelum mengubah, lalu edit file live itu (jangan generate ulang menimpa).

## Motion carousel (page "Carousel Motion")

- Video per slide 1080×1350, 24 fps, 7 dtk, loop mulus. **Tanpa transisi**: desain lengkap dari frame pertama, yang bergerak hanya karakter.
- Karakter dianimasikan lewat rig per frame, **animate on 2s** (`video/src/charAnim.tsx`), semua gerak berperiode 7/n dtk.
- Pipeline: `python3 src/motion_carousel.py video/src/slides-pXX.ts <slide.dc.html>...` → komposisi di `video/src/Root.tsx` → render Remotion.

## Rig karakter

- Celana pendek anak laki-laki bertulang (ikut paha). Rok pendek melebar mengikuti kaki.
- Rok panjang berhijab dan rok tentor: kaki tidak digambar (hanya sepatu), ujung rok ikut kaki: aurat selalu tertutup.
- `char/Figure.tsx` sumber utama; salin ke `video/src/rigv3/Figure.tsx` setiap ada perubahan.
