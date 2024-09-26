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

![2b1](https://github.com/user-attachments/assets/522816df-fa86-4398-9600-cbd17d6eb00b)



**3.   Logout**

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 

Echo “Terima kasih atas sesi yang diberikan”  
Sleep 5  
clear 

![3a](https://github.com/user-attachments/assets/2f36d7e5-af10-4d91-9505-d6f2827394d3)

![3b](https://github.com/user-attachments/assets/047a5c2f-f1a9-4a27-8ed3-bdc171186b4f)


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

![4a](https://github.com/user-attachments/assets/9ccf52da-9ceb-4386-a931-d7a5fa7a26ab)

![4a (1)](https://github.com/user-attachments/assets/e61d7ba6-74ac-4b32-a8b6-9afeb51c9309)

![4a (2)](https://github.com/user-attachments/assets/85a4b41b-3776-4b06-8fe0-66e68858f370)

![4a (3)](https://github.com/user-attachments/assets/85dfe4cb-e37f-48db-a00c-0076b181e204)

![4a (4)](https://github.com/user-attachments/assets/5ce2b515-bd0d-4f60-b9ed-1292802e8038)

![4a (5)](https://github.com/user-attachments/assets/172e451c-ba4a-44cb-8c65-6e2aad4e8a82)

b. Jalankan script tersebut sebagai berikut :  
$  ./p1.sh ; ./p3.sh ; ./p2.sh  
$  ./p1.sh &  
$  ./p1.sh $ ./p2.sh & ./p3.sh &  
$  ( ./p1.sh ; ./p3.sh ) &  

![4b1](https://github.com/user-attachments/assets/ae082e29-7603-4eb1-aafe-fbb5c425ec03)

![4b2](https://github.com/user-attachments/assets/3cf91643-8514-4349-be96-52054adb613c)

![4b3](https://github.com/user-attachments/assets/4e58d66e-fbc1-45be-9c82-81d186055abb)

![4b4](https://github.com/user-attachments/assets/d2aaed8b-10b9-4e56-91cd-cc5161d106a9)

![4b5](https://github.com/user-attachments/assets/9da84617-6920-4f23-816b-232110f70080)

![4b6](https://github.com/user-attachments/assets/2b572a48-09ee-4849-9c2a-b09ccd5dc436)

![4b7](https://github.com/user-attachments/assets/5fe73728-35c0-4436-947d-bcb56d48e100)

![4b8](https://github.com/user-attachments/assets/cf21050d-7935-4900-ac80-2984f7e421f1)


**5. Jobs**

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. 

#!/bin/bash  
while [ true ]  
do  
date >> hasil  
sleep 10  
done  

![5a1](https://github.com/user-attachments/assets/a4020cd1-de69-483e-a14f-f50a4310ee0a)

![5a2](https://github.com/user-attachments/assets/52f33965-b9df-418e-8f1e-d0d3720bef92)
  
b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut : 

$ jobs  
$ find / -print > files 2>/dev/null &  
$ jobs

![5b](https://github.com/user-attachments/assets/4971c975-de6d-4204-98f5-12962aaa68c2)

![5b1](https://github.com/user-attachments/assets/ae838f57-0c08-48c6-bcdd-f4140c8d52ab)

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background 

$ fg %1  
$ bg 

![5c](https://github.com/user-attachments/assets/fb4f4517-a339-462d-af64-9d7030314a43)

d.  Stop program background dengan utilitas kil 

$ ps x  
$ kill [Nomor PID] 

![5d1](https://github.com/user-attachments/assets/8231cd94-d4fe-4772-87bd-7c53effe9d26)

![5d2](https://github.com/user-attachments/assets/d99bba28-ef8e-407e-afba-d1532152fac4)

![5d3](https://github.com/user-attachments/assets/bccd8625-3114-4420-bace-ef07fc0e2fa8)


**6. History**
a. Ganti nilai HISTSIZE dari 1000 menjadi 20  

$ HISTSIZE=20  
$ h  

![6a](https://github.com/user-attachments/assets/9368d959-0304-4bfd-b7bc-4d69f91e6fd6)

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan  

$ !-5  

![6b](https://github.com/user-attachments/assets/11ea3fe4-e84a-4396-b473-01ac08da2cf2)

c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  

$ !!  

![6c](https://github.com/user-attachments/assets/e96e9b8e-cbda-4ceb-9b22-a7c9e8fd5c38)

d.  Ulangi instruksi pada history bufer nomor 150  

$ !150 

![6d](https://github.com/user-attachments/assets/e2e3704d-2fe0-41a0-8cf9-610581e00bba)

e.  Ulangi instruksi dengan prefix “ls”  

$ !ls 

![6e](https://github.com/user-attachments/assets/442a7b17-38bb-414a-996d-9597918a4359)
