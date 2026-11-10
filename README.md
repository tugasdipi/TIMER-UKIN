# UKin Timer — UKPPG Calon Guru

Aplikasi timer pembelajaran universal, siap dipublikasikan menggunakan **GitHub Pages**. Berjalan langsung di browser tanpa npm, framework, basis data, atau server khusus.

## Isi proyek

```text
index.html                   # Halaman aplikasi utama
presets/diva-detail-28.json  # Preset Diva SAKUNALAR: detail 28 tahap, 80 menit
presets/diva-ringkas-7.json  # Preset Diva SAKUNALAR: ringkas 7 tahap, 80 menit
presets/bayu-80-menit.json   # Preset Bayu: perubahan iklim, 7 tahap, 80 menit
.nojekyll                    # Mencegah pemrosesan Jekyll yang tidak diperlukan
README.md                   # Petunjuk ini
```

**Catatan:** Semua file dalam GitHub Pages bisa diakses publik. Jangan mengunggah modul ajar lengkap atau dokumen yang memiliki informasi pribadi jika tidak ingin dipublikasikan. Paket ini **tidak** menyertakan file Word/PDF modul atau foto pribadi.

## Publikasi ke GitHub Pages (tanpa coding)

1. Masuk ke https://github.com lalu buat **repository baru** (contoh nama: `ukin-timer`). Untuk GitHub Free, gunakan repository **Public**.
2. Unduh berkas ZIP proyek dan **ekstrak** di komputer.
3. Di repository, pilih **Add file → Upload files**. Unggah **isi folder hasil ekstraksi** sehingga `index.html` berada di **root repository** dan folder `presets` juga berada di root; klik **Commit changes**. Jangan unggah ZIP sebagai satu file.
4. Pilih **Settings → Pages**.
5. Pada **Build and deployment**, pilih **Source: Deploy from a branch**.
6. Pilih **Branch: main** dan folder **/(root)**, lalu **Save**.
7. Setelah publikasi selesai, kunjungi `https://USERNAME.github.io/ukin-timer/` (ganti `USERNAME` dan nama repository).

Dokumentasi resmi: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Menggunakan preset Diva atau Bayu

- Buka **UKin Timer** melalui URL GitHub Pages.
- Di **Editor Tahapan**, pada baris **Preset Cepat** pilih **Diva · Detail (28 tahap)**, **Diva · Ringkas (7 tahap)**, atau **Bayu · 80 menit (7 tahap)**, lalu tekan **Muat**.
- Konfirmasi penggantian konfigurasi; timer akan berisi tahapan dan durasi sesuai modul.
- Tekan **Mode Fokus** dan **Layar Penuh** untuk pemantauan di kelas.
- Semua format waktu menggunakan **MM:SS** (80 menit = `80:00`), bukan jam:menit:detik.

**Penggunaan file offline:** buka `index.html` secara langsung di browser. Timer dan fitur edit tetap bekerja, tetapi **Preset Cepat** membutuhkan web server (termasuk GitHub Pages). Saat offline, unduh file `.json` dari folder `presets` dan gunakan tombol **Impor Konfigurasi** di editor.

## Memakai modul ajar lain

Buat/konversi konfigurasi `.json` berisi `moduleTitle`, `modelName`, `target`, dan daftar `stages` (setiap tahap `id`, `name`, `short`, `cue`, `minutes`). Gunakan tombol **Impor Konfigurasi**. Format kompatibel dapat dibuat dari **Simpan Konfigurasi (.json)**.

> Perubahan konfigurasi yang dilakukan lewat browser disimpan hanya di browser/perangkat tersebut. Data **tidak otomatis tersinkron** ke GitHub atau antarperangkat. Untuk mencadangkan atau berpindah perangkat, pilih **Simpan Konfigurasi (.json)** lalu impor kembali. Tidak ada database dan tidak ada pengunggahan data peserta didik.

## Pembaruan situs

Setiap kali `index.html` atau `presets/*.json` diubah, unggah versi terbaru ke repository dan commit. GitHub Pages akan mempublikasikan versi terbaru. Jika tampilan belum berubah, lakukan refresh browser.
