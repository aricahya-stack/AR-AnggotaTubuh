# AR Wajah Kelas

Aplikasi web baru untuk demonstrasi deteksi wajah, label AR, pengenalan wajah, dan penyimpanan biometrik di Supabase. **Terpisah dari proyek Ular Tangga**; pasang sebagai repo dan proyek Supabase yang berbeda.

- Kamera dan model Human/TensorFlow.js berjalan di browser. Model BlazeFace, FaceMesh, dan FaceRes disertakan di `public/models/`; tidak mengambil bobot dari CDN.
- Pengajar mendaftarkan peserta yang setuju, tiga sampel per orang. Kamera tidak merekam atau menyimpan foto/video; embedding wajah **tetap merupakan data biometrik** dan dikirim terenkripsi lewat HTTPS untuk disimpan di Supabase.
- Supabase Auth hanya untuk pengajar. Function `/api/face` memeriksa token dan `INSTRUCTOR_EMAIL` sebelum mengakses tabel privat. Mahasiswa tidak perlu membuat akun.
- SQL dipisah menjadi `01_tabel.sql`, `02_akses.sql`, dan `03_pencocokan.sql`. Data bisa dihapus melalui aplikasi.

Mulai dari **[README-INSTALASI.md](README-INSTALASI.md)**. Rancangan pertemuan tersedia di **[PANDUAN-KULIAH.md](PANDUAN-KULIAH.md)**.

Teknologi: Vite, TypeScript, Human (TensorFlow.js), Bootstrap Icons, Supabase Auth + PostgreSQL/pgvector, Vercel Functions.

> Demonstrasi ini bukan sistem presensi, keamanan pintu, atau verifikasi identitas resmi. Ambang kemiripan harus diuji dengan peserta yang setuju, perangkat yang akan dipakai, dan pencahayaan kelas. Menggerakkan kepala saat pendaftaran bukan uji anti-pemalsuan yang kuat.
