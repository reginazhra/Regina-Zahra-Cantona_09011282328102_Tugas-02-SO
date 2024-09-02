# PRAKTIKUM 1 DAN 2 - INSTALASI SISTEM OPERASI LINUX 

# 1. Proses Instalasi
Gambar dibawah ini menunjukkan bahwa instalasi sistem operasi linux/ubuntu di vmware berhasil mengikuti prosedur yang ada dan untuk login ke linux memerlukan katasandi
![Screenshot 2024-09-02 143055](https://github.com/user-attachments/assets/819a3eeb-bb6b-47da-a884-fc45bb39c8ca)
![Screenshot 2024-08-29 150221](https://github.com/user-attachments/assets/aaba3de3-2da4-47a5-bce8-a6cbda02b360)
Berikut tampilan setelah memasukan kata sandi kedalam ubuntu
![Screenshot 2024-08-29 145303](https://github.com/user-attachments/assets/2f118429-4d82-4374-a519-c0d5bf657dac)

# 2. Analisis "/" pada opsi Mount Point
Kita perlu memilih "/" sebagai Mount Point saat instalasi karena tanda "/" ini adalah simbol untuk direktori root, alias tempat utama di mana semua file sistem Linux disimpan. Ketika kita instal Ubuntu atau sistem operasi lain, kita harus menentukan di mana file utama ini akan diletakkan. Dengan memilih "/" sebagai Mount Point, kita memberitahu sistem untuk menempatkan semua file penting di partisi ini. Intinya, memilih "/" itu penting karena itulah tempat semua file inti dari sistem operasi akan disimpan, sehingga sistem bisa berjalan dengan baik setelah instalasi selesai. Kalau tidak kita pilih, sistem bisa bingung mau meletakkan file di mana, dan ini bisa bikin instalasi gagal atau sistem jadi tidak lengkap.

# 3.	Berikan penjelasan tentang ext4, ext3, swap, ntfs, fat32, btrfs!
•	ext4 (Fourth Extended File System)
- Penggunaan: Umumnya digunakan di sistem Linux.
- Kelebihan: Menyediakan fitur seperti journaling, yang meningkatkan keandalan data dengan menyimpan perubahan pada log sebelum menulis ke disk. Mendukung volume dan ukuran file yang sangat besar.   
- Kekurangan: Meskipun stabil, tidak memiliki beberapa fitur canggih yang ada pada sistem file modern seperti Btrfs.

•	ext3 (Third Extended File System)
- Penggunaan: Juga digunakan di sistem Linux.
- Kelebihan: Memperkenalkan fitur journaling untuk meningkatkan keandalan data. Lebih stabil dibandingkan ext2, tetapi tidak seefisien ext4.
- Kekurangan: Tidak mendukung ukuran file dan volume sebesar ext4 dan tidak secepat ext4 dalam hal kinerja.

•	swap 
- Penggunaan: Berfungsi sebagai area penyimpanan tambahan untuk RAM di sistem Linux.
- Kelebihan: Membantu sistem untuk menjalankan aplikasi lebih besar dari kapasitas RAM yang tersedia dengan menyimpan data sementara di disk.
- Kekurangan: Akses ke swap lebih lambat dibandingkan RAM, sehingga kinerja sistem bisa terpengaruh jika terlalu bergantung pada swap.

•	ntfs (New Technology File System)
- Penggunaan: Sistem file utama untuk Windows NT dan sistem operasi yang lebih baru (seperti Windows 10/11).
- Kelebihan: Mendukung fitur seperti enkripsi, kompresi, dan hak akses file yang lebih canggih dibandingkan FAT32. Memungkinkan volume dan file yang sangat besar.
- Kekurangan: Kurang kompatibel dengan sistem operasi non-Windows, meskipun dukungan untuk baca/tulis NTFS ada di beberapa sistem Linux.

•	fat32 (File Allocation Table 32)
- Penggunaan: Sistem file yang lebih tua yang digunakan di berbagai sistem operasi, termasuk Windows, macOS, dan Linux.
- Kelebihan: Kompatibel dengan hampir semua sistem operasi, ideal untuk perangkat penyimpanan portabel seperti USB flash drive.
- Kekurangan: Tidak mendukung file yang lebih besar dari 4 GB dan volume lebih besar dari 8 TB. Tidak memiliki fitur seperti journaling.

•	btrfs (B-tree File System)
- Penggunaan: Sistem file yang relatif baru untuk Linux, dirancang untuk menggantikan ext4.
- Kelebihan: Menawarkan fitur canggih seperti snapshot, pengendalian kesalahan, dan kompresi data. Fleksibel dan mendukung pengelolaan volume yang lebih kompleks.
- Kekurangan: Masih dianggap kurang stabil dibandingkan ext4 dan mungkin tidak selalu cocok untuk semua jenis penggunaan.

