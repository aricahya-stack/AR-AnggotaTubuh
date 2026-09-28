# Panduan demo di kelas

## Hasil belajar

Mahasiswa dapat menjelaskan empat hal: (1) kamera memperoleh video, (2) model menemukan posisi wajah, (3) model membuat embedding berupa angka, (4) Supabase menyimpan dan mencari data. Setelah membuka satu URL, mahasiswa melihat label AR bergerak mengikuti wajah dan riwayat muncul di database.

## Persiapan dosen (sebelum mahasiswa masuk)

1. Pastikan tiga query SQL, Vercel, email pengajar, dan model kamera telah diuji di ponsel yang akan dipakai.
2. Pilih 2–4 sukarelawan dewasa yang memahami tujuan demo dan setuju. Siapkan kondisi terang. Orang lain dapat menjadi contoh "tidak dikenal" tanpa disimpan.
3. Gunakan **satu perangkat yang dioperasikan pengajar** untuk pendaftaran agar kunci dan akun tidak dibagikan. Siapkan layar kedua dengan Supabase Table Editor pada `face_profiles` dan `face_events`.
4. Ingatkan kelas bahwa skor kemiripan adalah hasil model, bukan bukti identitas; wajah kembar, foto, kondisi cahaya, dan perangkat bisa memengaruhi hasil.

## Pertemuan 1 — Kamera dan AR

- Tunjukkan tombol kamera dan izin akses di browser.
- Tampilkan bingkai serta titik wajah; minta sukarelawan menggerakkan kepala untuk melihat label ikut bergerak.
- Jelaskan fungsi `getUserMedia`, model wajah, koordinat kotak, dan Canvas.
- Coba kondisi tidak terdeteksi dan dua wajah untuk menunjukkan batas sistem.

## Pertemuan 2 — Pendaftaran dan database

- Buka tab **Daftarkan Wajah**; sebutkan persetujuan sebelum menyimpan.
- Ambil tiga sampel berbeda dan tunjukkan nama peserta di Supabase Table Editor.
- Jelaskan perbedaan `face_profiles`, `face_samples`, dan `face_events`; sambungkan ke konsep relasi dan foreign key.
- Minta mahasiswa memprediksi hasil kamera untuk orang yang baru dan yang sudah terdaftar.

## Pertemuan 3 — Pengenalan dan pengujian

- Tunjukkan proses pencarian kandidat terdekat dan slider kemiripan.
- Uji orang terdaftar, orang lain yang belum didaftar, dan penerangan berbeda.
- Perlihatkan riwayat; ubah ambang dan diskusikan salah cocok serta tidak cocok.
- Hapus profil atas permintaan sukarelawan dan amati efeknya pada tabel sampel/riwayat.

## Tugas mahasiswa

Modifikasi satu bagian berikut: tampilkan kosakata Arab untuk mata/hidung/mulut, jelaskan mengapa gambar wajah tidak perlu disimpan, buat visualisasi jumlah pencocokan per kelas, atau tambahkan pengujian beberapa tingkat cahaya. Penilaian menekankan pemahaman alur dan keterbatasan model, bukan memaksimalkan pengumpulan data wajah.
