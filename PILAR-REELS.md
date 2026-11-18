# Pilar Reels Prestama (3× seminggu)

Semua Reels: 1080×1920, 30 fps, aman untuk Reels dan Story (konten penting di y 260–1580, kanan bawah kosong untuk ikon),
VO Siti lewat ai33 satu take, timing kata dari ElevenLabs forced alignment, −14 LUFS.
Pembuka dan CTA berlatar oranye tanpa subtitle; bagian penjelasan berlatar cream dengan subtitle blur ala Apple (biru gelap, maks 4 kata).
Komponen bersama: `video/src/kit.tsx` (header, subtitle, tombol Follow, musik, SFX).

| Hari | Pilar | Label header | Isi | Contoh |
|---|---|---|---|---|
| Senin | **Tips Ngajar di Rumah** | `TIPS NGAJAR #N` | Semi-parenting tapi akademik: cara Bunda menemani anak belajar satu materi. Hook masalah → contoh soal → 3 langkah → ringkasan → CTA simpan + follow | `TipsNgajar01.tsx` (soal cerita) |
| Kamis | **Bahas Soal** | `BAHAS SOAL #N` | Template final di `CLAUDE.md`. Pasangan Tantangan feed hari Rabu | `BahasSoal03.tsx` |
| Sabtu | **Trik Kilat** | `TRIK KILAT #N` | ±35 dtk, satu trik, **3 contoh** demo close-up (penanda ●●●), CTA: coba soal di komentar + follow | `TrikKilat01.tsx` (perkalian 9 pakai jari: 9×3, 9×7, 9×9) |

Satu tema per minggu menyatukan ketiganya (Minggu 2: soal cerita).
Soal cerita (di pilar mana pun) selalu diberi adegan cerita beranimasi saat soalnya dibacakan: `video/src/story.tsx`
(`RaniStory` untuk Tips Ngajar #1, `IbuStory` untuk Bahas Soal #3).
Nada selalu positif: tidak menyalahkan orang tua atau anak. Jangan pakai kata "hayo" di VO (pelafalannya aneh).

## Produksi

```bash
cd video/vo && python3 make_vo.py <folder-episode>   # lines.json + script.txt -> raw.mp3, timing.json, vo.wav
```
Salin `vo.wav` ke `video/public/vo-<ep>.wav` dan `timing.json` ke `video/src/timing-<ep>.json`, daftarkan komposisi di `Root.tsx`, lalu render
dan normalisasi seperti di `README.md`.

## Kredit ai33 (VO Siti)
| Episode | Kredit |
|---|---|
| Tips Ngajar #1 | 864 |
| Bahas Soal #3 | 807 |
| Trik Kilat #1 | 422 (v1) + 526 (v2, 3 contoh) |
| CTA Bahas Soal tanpa "hayo" (disambung ke #1–#3) | 78 |
