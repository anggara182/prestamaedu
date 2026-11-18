# Pilar baru: BAHAS SOAL (motion video explainer)

Reels/TikTok 9:16 yang membahas satu soal sampai tuntas dengan animasi.
Tag seri di kiri atas: `BAHAS SOAL #N`.

## Kenapa pilar ini

- **Konten yang paling dicari ortu murid kelas 6 dan 9 menjelang TKA.** Jalan sampai April 2027.
- **Video mendorong jangkauan ke non-follower.** Feed carousel lebih bagus untuk disimpan; keduanya saling melengkapi.
- **Menunjukkan value Prestama secara langsung.** Satu soal dibahas dengan dua cara, sesuai gaya belajar yang berbeda. Penonton melihat sendiri kenapa metode personal itu penting.

## Format

| | |
|---|---|
| Ukuran | 1080×1920, 30–60 detik |
| Visual | Motion graphic 100% kode (SVG), karakter dan palet Prestama, tanpa gambar AI |
| Suara | VO tentor asli (paling dipercaya ortu) atau TTS sebagai cadangan |
| Teks | Subtitle per kata, kata kunci di kotak oranye; aman dibaca tanpa suara |
| Frekuensi | 2× seminggu |

## Struktur 6 beat

1. **Hook (0–3 dtk):** soal dan jebakannya langsung di layar. Contoh: "Banyak yang jawab 2¼ kg. Padahal salah."
2. **Soal (3–8 dtk):** soal utuh dan pilihan jawaban, cukup lama untuk dibaca.
3. **Cara 1, visual (8–25 dtk):** diagram animasi, misalnya batang pecahan.
4. **Cara 2, praktik (25–40 dtk):** benda nyata, misalnya gelas takar di dapur. Langsung masuk ("Cara kedua. Ambil…"), tanpa kalimat pengantar.
5. **Jawaban + trik cepat (40–50 dtk):** jawaban dan satu kalimat trik yang mudah diingat.
6. **CTA (±5 dtk):** "Jawabanmu tadi bener nggak? Follow biar nggak ketinggalan materi lain!" Elemen minimal di tengah: judul + tombol Follow yang ditekan, karakter di bawah. Tanpa pill layanan, logo besar, atau slogan.

Aturan visual: karakter hanya di hook dan CTA, bagian pembahasan bersih tanpa karakter. Subtitle hanya di bagian pembahasan (latar terang). Layout aman untuk Reels dan Story.

## Alur mingguan

Rabu: post feed **Tantangan Prestama** (soal saja) → komentar masuk.
Kamis: Reels **Bahas Soal** untuk soal yang sama → orang balik untuk cek jawaban.
Minggu: Reels Bahas Soal kedua, topik dari permintaan di komentar.

| Hari | Pilar | Format |
|---|---|---|
| Senin | Motivasi | Single image |
| Selasa | Teman Belajar Bunda (tips ortu) | Carousel |
| Rabu | Tantangan Prestama | Single image |
| **Kamis** | **Bahas Soal** | **Reels** |
| Jumat | Kenali Gaya Belajar / interaktif | Single image |
| Sabtu | Info pendidikan / cerita kelas | Carousel |
| **Minggu** | **Bahas Soal** atau soft promo | **Reels** / single |

## Bank topik awal (soal dibuat sendiri mengikuti kisi-kisi, bukan menyalin soal resmi)

**Matematika SD:** pecahan campuran, KPK dan FPB dalam cerita, keliling dan luas gabungan bangun, debit, skala peta, rata-rata, membaca diagram.
**Bahasa Indonesia SD:** ide pokok paragraf, kalimat utama, simpulan teks, makna kata dalam konteks, kalimat efektif.
**SMP:** perbandingan, persamaan linear satu variabel, peluang sederhana, teks argumentasi.

## Episode 1 (storyboard)

Soal dari post Tantangan #1: *Ibu membeli 2½ kg gula, memakai ¾ kg. Sisa?* Jawaban B, 1¾ kg.

| Detik | Layar | VO |
|---|---|---|
| 0–3 | Karung gula 2½ kg, teks besar "2½ − ¾ = ?" dan cap merah di atas "2¼ kg?" | "Banyak yang jawab 2¼. Padahal salah." |
| 3–8 | Kartu soal dan 4 pilihan | "Ibu beli 2½ kilo gula, dipakai ¾ kilo. Sisanya berapa?" |
| 8–24 | Batang: 2½ kg dipecah jadi 10 kotak seperempat, 3 kotak menghilang, sisa 7 kotak | "Ubah dulu ke perempat. 2½ itu 10 perempat. Dipakai 3, sisa 7 perempat." |
| 24–38 | Karakter murid menuang gula ke 10 gelas takar kecil, 3 gelas diambil | "Kalau anakmu lebih paham lewat praktik, pakai gelas takar di dapur." |
| 38–48 | 7/4 berubah jadi 1¾, pilihan B menyala | "7 perempat sama dengan 1¾ kilo. Jawabannya B." |
| 51–56 | "Jawabanmu tadi bener nggak?" di tengah, tombol Follow berubah jadi Following, tentor dan murid di bawah | "Jawabanmu tadi bener nggak? Follow biar nggak ketinggalan materi lain!" |

Caption: hook + "Simpan buat latihan TKA" + pertanyaan komentar + 3 hashtag (`#BahasSoal #TKA2027 #LesPrivatSD`).

## Produksi (episode 1)

- VO: ai33, suara **Siti** (`elevenlabs_WAotVoK2Yv2ufjocfYYs`), speed 1.05, satu take untuk seluruh naskah agar natural.
  Timing per kata dari ElevenLabs forced alignment. Biaya ai33: 992 + 132 + 850 kredit (revisi naskah cara 2 dan CTA).
- Musik: ElevenLabs Music, instrumental ceria (ukulele, glockenspiel, marimba), di-duck otomatis di bawah VO.
- Render: Remotion `video/`, output `output/video/bahas-soal-01.mp4`, loudness −14 LUFS.
- Ikuti aturan antrean ai33 bersama (cek task pending, jarak submit ≥15 detik).
