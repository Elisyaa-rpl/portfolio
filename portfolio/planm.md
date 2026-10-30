# Rencana Pembenahan Portfolio Elisya

## Tujuan

Merapikan halaman portfolio Elisya menjadi website satu halaman yang terasa seperti suasana laut, menggunakan palet biru sea, tetap nyaman di desktop maupun perangkat mobile, dan memiliki animasi ikan yang halus di latar hero.

## Kondisi Saat Ini

- `index.html` sudah menggunakan Bootstrap, tetapi navigasinya masih berisi tautan contoh dan beberapa section belum memiliki isi.
- Hero memakai teks sementara dan path gambar yang belum tersedia.
- Project dan certificate masih berupa card placeholder dengan struktur HTML yang belum lengkap/rapi.
- `style.css` tersedia tetapi belum dimuat oleh halaman.
- Belum ada aturan desain, perilaku responsif khusus, atau animasi.

## Rencana Implementasi

1. **Rapikan struktur HTML**
   - Gunakan bahasa dokumen yang sesuai dengan konten berbahasa Indonesia.
   - Hubungkan `style.css` dari `<head>` dan rapikan hierarki elemen serta indentasi.
   - Gunakan elemen semantik seperti `header`, `nav`, `main`, `section`, dan `footer`.
   - Ganti tautan navigasi contoh dengan anchor ke section yang benar, misalnya Beranda, Tentang, Proyek, Sertifikat, dan Kontak.
   - Rapikan markup card proyek/sertifikat; hilangkan atribut inline dan sumber gambar placeholder yang tidak valid.
   - Gunakan CSS grid/flex di stylesheet proyek agar layout dan komponen tetap ringan tanpa ketergantungan Bootstrap.

2. **Terapkan tema biru sea**
   - Definisikan warna melalui CSS custom properties agar mudah dirawat: navy laut untuk kontras, beberapa tingkat biru/teal sebagai warna utama, serta putih atau warna pasir lembut sebagai warna netral.
   - Terapkan warna secara konsisten pada latar section, teks, tombol, navigasi, card, border, dan state hover/focus.
   - Pastikan teks dan tombol memiliki kontras yang memadai dan tetap mudah dibaca.

3. **Bangun ulang hero section**
   - Buat komposisi pembuka yang jelas: nama/identitas Elisya, perkenalan singkat, dan tombol menuju proyek atau kontak.
   - Gunakan ruang visual untuk foto/ilustrasi hanya jika aset yang benar tersedia; jangan meninggalkan broken image.
   - Tambahkan dekorasi laut berlapis yang tidak menghalangi keterbacaan konten.

4. **Tambahkan animasi ikan di latar hero**
   - Buat beberapa siluet ikan sebagai elemen dekoratif menggunakan SVG inline atau bentuk CSS sederhana, lalu animasikan gerakan berenang melintasi hero dengan keyframes.
   - Variasikan ukuran, kedalaman, arah, durasi, dan jeda animasi agar gerakannya terasa alami, tidak seragam, dan tidak mengganggu.
   - Letakkan ikan di belakang konten, non-interaktif, serta sembunyikan dari teknologi bantu (`aria-hidden`).
   - Batasi animasi pada hero dan gunakan transform/opacity agar gerakan tetap ringan.
   - Sediakan fallback `prefers-reduced-motion: reduce` untuk mengurangi atau menghentikan gerakan.

5. **Pastikan responsivitas**
   - Gunakan grid/flex yang fleksibel dan ukuran teks/spasi yang menyesuaikan viewport.
   - Pada layar kecil, susun hero dan konten secara vertikal; pastikan navigasi dapat digunakan dengan nyaman.
   - Buat card proyek/sertifikat mengalir dari beberapa kolom di desktop menjadi satu kolom pada ponsel tanpa overflow horizontal.
   - Uji breakpoint sempit, tablet, dan desktop; pastikan ornamen ikan tidak menutupi tombol atau teks.

6. **Lengkapi section portfolio**
   - Atur section Tentang, Proyek, Sertifikat, dan Kontak agar memiliki judul dan pola visual konsisten.
   - Pertahankan isi yang memang sudah tersedia; gunakan placeholder teks yang jelas hanya untuk informasi portfolio yang belum diberikan.
   - Tambahkan footer ringkas dan tautan kontak hanya jika alamat/akun yang benar tersedia.

## Verifikasi

- Periksa halaman pada viewport mobile, tablet, dan desktop.
- Pastikan tautan navigasi berpindah ke section yang sesuai dan menu mobile yang dibuat khusus tetap berfungsi.
- Pastikan tidak ada gambar rusak, markup yang tidak valid, horizontal scrolling, atau elemen yang saling menutupi.
- Periksa animasi ikan berjalan halus, tetap berada di belakang konten, dan mengikuti preferensi reduced motion.
- Periksa kontras, fokus keyboard, teks alternatif aset informatif, dan aksesibilitas elemen dekoratif.

## Batasan

- Rencana ini sudah diterapkan pada `index.html` dan `style.css`.
- Foto, deskripsi diri, daftar proyek/sertifikat, serta tautan media sosial/kontak perlu memakai aset dan data Elisya yang benar, bukan dibuat-buat.
- Teks proyek dan sertifikat saat ini ditandai sebagai contoh agar bisa diganti dengan informasi yang akurat.
