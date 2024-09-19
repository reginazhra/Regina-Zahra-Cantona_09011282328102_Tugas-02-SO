# TUGAS 4 LAPORAN PRAKTIKUM 4
1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard 
output ke file baru. 
 Untuk melihat daftar direktori aktif, gunakan perintah $ ls, sedangkan 
untuk membelokkan tampilan standard output ke file baru, gunakan ‘>’ 
![Screenshot 2024-09-19 081254](https://github.com/user-attachments/assets/17661a2d-16bf-4355-963b-27a9ed6d3839)

2. Lihat daftar secara lengkap pada direktori /etc/passwd, belokkan tampilan 
standard output ke file baru tanpa menghapus file baru sebelumnya. 
 Untuk melihat daftar lengkap dari direktori /etc/passwd, gunakan perntah 
$ ls, sedangkan untuk membelokkan tampilan standard output ke file baru 
tanpa menghapus file baru sebelumnya, gunakan ‘>>’
![Screenshot 2024-09-19 081346](https://github.com/user-attachments/assets/e99c3e12-818a-4b39-ae9f-b61515e4afc8)

3. Urutkan file baru dengan cara membelokkan standard input. 
 Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk 
membelokkan standard input, gunakan ‘<’
![Screenshot 2024-09-19 081406](https://github.com/user-attachments/assets/9eb9ce79-34eb-4c4c-afeb-8c1997304d78)

4. Lihat Urutkan file baru dengan cara membelokkan standard input dan standard 
output ke file baru.urut. 
➢ Untuk mengurutkan file, gunakan perintah $ sort, sedangkan untuk 
membelokkan standard input, gunakan ‘<’, sedangkan untuk membelokkan 
standard output ke file, gunakan ‘>’. Pembelokan standart input dan standart 
output dapat dikombinasikan asalkan tidak boleh menggunakan nama file yang 
sama sebagai standart input dan output
![Screenshot 2024-09-19 081425](https://github.com/user-attachments/assets/5a7a4268-5b62-45c9-afac-753db1c321e5)

5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file 
rmdirerror.txt. 
 Gunakan perintah $ mkdir untuk membuat direktori baru. Saat membuat 
direktori yang sama sebanyak dua kali, akan muncul pesan error. Pesan 
error itu kemudian dibelokkan ke file dengan menggunakan ‘2>’
![Screenshot 2024-09-19 081500](https://github.com/user-attachments/assets/2411581e-c121-4c9f-91b6-b6dfd5d2a391)

6. Urutkan kalimat berikut : 
Jakarta 
Bandung 
Surabaya 
Padang 
Palembang 
Lampung 
Dengan menggunakan notasi here document (<@@@ ...@@@) 
 Pertama, buat notasi here document yang akan dibelokkan ke sebuah file 
kemudian isi document tersebut. Setelah diisi dan diakhiri, isi dokumen 
akan tersimpan ke file yang dibelokkan. File tersebut kemudian diurutkan 
menggunakan perintah $ sort.
![Screenshot 2024-09-19 081525](https://github.com/user-attachments/assets/3f764ac8-77ff-4cd5-a819-42e555905cae)

7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan 
filter dan tambahkan data tersebut ke file baru. 
 Untuk mendapatkan jumlah baris, kata, dan karakter (secara berurutan) 
dari sebuah file, gunakan perintah wc yang dipipakan dengan perintah cat. 
Hasilnya kemudian bisa ditambahkan ke file menggunakan ‘>>’
![Screenshot 2024-09-19 081601](https://github.com/user-attachments/assets/809bbd87-b0a7-4e67-a99f-ffe0d16d8e5f)

8. Gunakan perintah di bawah ini dan perhatikan hasilnya. 
$ cat /etc/passwd | sort | pr –n | grep tty03  
$ find /etc –print | head  
$ head /etc/passwd | tail –5 | sort
![Screenshot 2024-09-19 081625](https://github.com/user-attachments/assets/a1b7769a-5ac6-48cf-828b-eb58f90996e6)

9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.
![Screenshot 2024-09-19 081643](https://github.com/user-attachments/assets/b7fe0e98-1cfb-438a-8e23-ec7459f2d8bf)





