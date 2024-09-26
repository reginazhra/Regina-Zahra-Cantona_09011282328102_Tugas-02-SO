# LAPORAN PRAKTIKUM 6 SISTEM OPERASI 
## JOB CONTROL 

<h2/>1.  Eksekusi seluruh profil yang ada:<h2/>

a.  Edit file profil `/etc/profile` dan tampilkan pesan sebagai berikut:  </h2> <bahasa inggris/>
echo “Profile dari /etc/profile” <bahasa inggris/>
  
![Screenshot 2024-09-25 231857](https://github.com/user-attachments/assets/95b9a72c-ec87-4364-8fca-eb3b8cd1f7ea)
![Screenshot 2024-09-25 231519](https://github.com/user-attachments/assets/8741f33f-a839-42d0-824f-922700fbd3e4)

b.  Asumsi nama Anda `stD02001`, maka edit semua profil yang ada yaitu:  
/home/stD02001/.bash_profile <bahasa inggris/>
  
/home/.stD02001/.bash_login <bahasa inggris/>

/home/mahasiswa/.profile  <bahasa inggris/>

/home/mahasiswa/.bashrc <bahasa inggris/>

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/mahasiswa/.bash_profile : 

echo “Profile dari .bash_profile” 

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. 
![Screenshot 2024-09-26 013442](https://github.com/user-attachments/assets/5cec8acb-573b-4ba7-90a9-44f63d3f4510)
![Screenshot 2024-09-25 152708](https://github.com/user-attachments/assets/ce656985-a334-4752-8815-4204ed83cf66)
![Screenshot 2024-09-25 152922](https://github.com/user-attachments/assets/2f555e47-e69c-4119-9bdf-b13473758843)
![Screenshot 2024-09-25 153408](https://github.com/user-attachments/assets/997d7253-4b1a-4885-8804-2713126cc253)
![Screenshot 2024-09-26 021211](https://github.com/user-attachments/assets/d2d0f055-b690-47d8-abbe-39ed15ac2c06)


c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:
 
$ su mahasiswa 
$ exit

![Screenshot 2024-09-26 021648](https://github.com/user-attachments/assets/bb8144fd-1634-4a6b-8bf7-b1daa263a62a)

kemudian gunakan opsi – sebagai berikut : 

$ su – mahasiswa  
$ exit

![Screenshot 2024-09-26 021847](https://github.com/user-attachments/assets/bf8bb739-64a9-48bd-923c-d8fcb19fd70a)



Jelaskan perbedaan kedua utilitas tersebut.  
1. su mahasiswa:  
Perintah su mahasiswa digunakan untuk beralih ke akun pengguna bernama "mahasiswa" tanpa mengubah lingkungan shell secara penuh. Dalam hal ini, hanya identitas pengguna yang berubah, tetapi variabel lingkungan (seperti $PATH, alias, dan pengaturan shell lainnya) tetap milik pengguna saat ini. Ini berarti beberapa program atau perintah mungkin tidak berfungsi dengan benar karena masih menggunakan konfigurasi dari pengguna asli.

2. su - mahasiswa:   
Sedangkan su - mahasiswa tidak hanya mengubah identitas pengguna, tetapi juga memulai sesi shell baru seperti halnya ketika pengguna "mahasiswa" masuk secara langsung. Semua variabel lingkungan akan direset sesuai dengan pengaturan default pengguna "mahasiswa", termasuk $HOME, $PATH, dan lainnya. Ini memberikan pengalaman yang lebih lengkap dan aman, seolah-olah Anda baru saja login sebagai "mahasiswa".


**2. Prompt String (PS)** 

a.  Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
PS1=‟> „  
export PS1 

![Screenshot 2024-09-26 022139](https://github.com/user-attachments/assets/88e5a0e0-3dd2-4f3f-9ede-6d24ff570014)

![Screenshot 2024-09-26 084623](https://github.com/user-attachments/assets/9998d939-83c7-4ece-ab6d-4ff823e0a712)

b.  Eksperimen hasil PS1 : 

$ PS1=“\! > “  
69 > PS1=”\d > “  
Mon Sep 23 > PS1=”\t > “  
10:10:20 > PS1=”Saya=\u > “  
Saya=mahasiswa > PS1=”\w >”  
~ > PS1=\h >”

![Screenshot 2024-09-26 115642](https://github.com/user-attachments/assets/53831ca9-83bb-4c45-ac19-9038d176d6aa)


**3.   Logout**

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 

Echo “Terima kasih atas sesi yang diberikan”  
Sleep 5  
clear 

![Screenshot 2024-09-26 120336](https://github.com/user-attachments/assets/e6008afd-3d5d-43da-8913-c7862a56dae6)

![Screenshot 2024-09-26 121800](https://github.com/user-attachments/assets/25b801ee-c281-4e98-b028-35f0d7654a2b)


**4. Bash script**

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

p1.sh  
#! /bin/bash  
echo “Program p1”  
ls –l  
p2.sh  
#! /bin/bash  
echo “Program p2”  
who  
p3.sh  
#! /bin/bash  
echo “Program p3”  
ps x  

![Screenshot 2024-09-26 130502](https://github.com/user-attachments/assets/4558e7cc-bad9-4346-97df-4ba59934e82f)

![Screenshot 2024-09-26 130339](https://github.com/user-attachments/assets/a20fbed5-9a4a-4911-b655-7eff12c82d17)

![Screenshot 2024-09-26 124718](https://github.com/user-attachments/assets/731b80a4-7a4d-49cd-8b74-a126f64d3c96)

![Screenshot 2024-09-26 124540](https://github.com/user-attachments/assets/707ef400-96f7-4caf-b0ac-02b12d9f7209)

![Screenshot 2024-09-26 125110](https://github.com/user-attachments/assets/9d579c08-9bac-48b5-828f-192bac4fd0d3)

![Screenshot 2024-09-26 125050](https://github.com/user-attachments/assets/91a0c000-7df0-4c6f-bd67-eab231219044)

b. Jalankan script tersebut sebagai berikut :  
$  ./p1.sh ; ./p3.sh ; ./p2.sh  
$  ./p1.sh &  
$  ./p1.sh $ ./p2.sh & ./p3.sh &  
$  ( ./p1.sh ; ./p3.sh ) &  

![Screenshot 2024-09-26 125612](https://github.com/user-attachments/assets/0d456ec8-a43a-4476-bc6c-733918ea7506)

![Screenshot 2024-09-26 131545](https://github.com/user-attachments/assets/56c11d88-59d5-4dad-a38b-b45ee64ada03)

![Screenshot 2024-09-26 131714](https://github.com/user-attachments/assets/e5ea07a1-8f49-4bda-9054-218465a44422)

![Screenshot 2024-09-26 131806](https://github.com/user-attachments/assets/5f93417f-5723-4bca-9d9a-b1d7f49d4a52)

![Screenshot 2024-09-26 132053](https://github.com/user-attachments/assets/7be91615-5672-4ce3-9f48-36f984ee934c)

![Screenshot 2024-09-26 132500](https://github.com/user-attachments/assets/4549ac05-cf06-45ae-9f95-db6d78de4719)

![Screenshot 2024-09-26 132601](https://github.com/user-attachments/assets/e14f7e37-bd16-469a-b249-644efc005254)

![Screenshot 2024-09-26 132859](https://github.com/user-attachments/assets/42f4d05e-ea3a-43cb-800d-7d567ca51460)

![Screenshot 2024-09-26 132953](https://github.com/user-attachments/assets/b5a16f92-84db-4cef-aa89-2bf0220c763c)


**5. Jobs**

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. 

#!/bin/bash  
while [ true ]  
do  
date >> hasil  
sleep 10  
done  

![Screenshot 2024-09-26 133305](https://github.com/user-attachments/assets/9e283b8a-7d0d-41af-824f-a9e4a7be060f)

![Screenshot 2024-09-26 133249](https://github.com/user-attachments/assets/aaa1299a-3c9f-47c4-ae92-ddab4e4b59dc)
  
b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut : 

$ jobs  
$ find / -print > files 2>/dev/null &  
$ jobs

![Screenshot 2024-09-26 135755](https://github.com/user-attachments/assets/d28ac2de-6753-403f-94de-2e795dfd1583)

![Screenshot 2024-09-26 140009](https://github.com/user-attachments/assets/2be5509f-8dbf-4399-a993-d3fdbb8c954d)

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background 

$ fg %1  
$ bg 

![Screenshot 2024-09-26 140438](https://github.com/user-attachments/assets/59b38bd5-c68a-4baa-b81f-115a600aa4b8)

d.  Stop program background dengan utilitas kil 

$ ps x  
$ kill [Nomor PID] 

![Screenshot 2024-09-26 140639](https://github.com/user-attachments/assets/84ab09b5-7bb3-4175-a3e2-28a4c08eb848)

![Screenshot 2024-09-26 141007](https://github.com/user-attachments/assets/d8dc46f2-98ca-481b-99ad-b31def0eb62a)


**6. History**
a. Ganti nilai HISTSIZE dari 1000 menjadi 20  

$ HISTSIZE=20  
$ h  

![Screenshot 2024-09-26 142007](https://github.com/user-attachments/assets/07bf68dc-6694-4d84-9df9-8414c346e6c8)

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan  

$ !-5  

![Screenshot 2024-09-26 142139](https://github.com/user-attachments/assets/0fa3b876-93d8-4eea-b40b-1d0e258f1e8e)

c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  

$ !!  

![Screenshot 2024-09-26 142327](https://github.com/user-attachments/assets/012e1e1a-0676-4316-961e-2a6629e8919f)

d.  Ulangi instruksi pada history bufer nomor 150  

$ !150 

![Screenshot 2024-09-26 142551](https://github.com/user-attachments/assets/f67fae70-fd0a-4fb8-bf4f-997b8281332e)

e.  Ulangi instruksi dengan prefix “ls”  

$ !ls 

![Screenshot 2024-09-26 142724](https://github.com/user-attachments/assets/3664899a-7c12-4680-aee5-ef144ee62764)
