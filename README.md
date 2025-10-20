![alt text](https://a.top4top.io/p_3580f7uhc1.png?raw=true)
![alt text](https://b.top4top.io/p_3580qsvqk2.png?raw=true)

Mass phpMyAdmin Finder adalah tools penetration testing yang powerful untuk menemukan instalasi phpMyAdmin yang ter-expose secara tidak sengaja. Tools ini membantu security researcher dan admin sistem untuk mengidentifikasi potensi celah keamanan dalam infrastruktur web.

✅ Apa saja yang dilakukan kode ini?
  - 🔍 Membaca daftar domain dari file teks (domains.txt atau sesuai input).
  - 📜 Membaca daftar path yang kemungkinan mengarah ke phpMyAdmin dari file data.txt.
  - 🌐 Melakukan request ke setiap domain + path untuk mencari tahu apakah ada instance phpMyAdmin yang aktif.
  - 🧠 Mendeteksi isi konten halaman untuk mengecek apakah itu benar phpMyAdmin.
  - 💾 Menyimpan hasilnya ke file (jika diminta).
  - 🧵 Menggunakan threading supaya proses scanning bisa lebih cepat (multi-threaded).
  - 📊 Menampilkan hasil scanning secara real-time di terminal.

📚 Class MassPhpMyAdminFinder

Ini adalah inti dari tool ini.
  - 🔃 __init__: Menyiapkan konfigurasi awal (baca file domain dan path, set timeout, dll).
  - 📂 load_domains(): Membaca daftar domain dari file.
  - 📂 load_wordlist(): Membaca daftar path dari file data.txt (misalnya: /phpmyadmin/, /pma/, dll).
  - 🔗 check_phpmyadmin(): Mengecek apakah kombinasi domain+path mengarah ke phpMyAdmin.
  - Menggunakan requests.get() ➡️ status 200 ✅ ➡️ cek konten apakah mengandung kata "phpmyadmin", dll.
  - 💾 save_to_file(): Menyimpan hasil yang ditemukan ke file output (jika diinputkan).
  - 🧵 scan_domain(): Melakukan scanning terhadap satu domain menggunakan thread.
  - 🚀 scan(): Fungsi utama untuk memulai proses scanning semua domain.
  - 🧾 show_summary(): Menampilkan ringkasan hasil scan.

