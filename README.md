# Jarkom-Modul-1-D19-2023
Laporan Resmi Praktikum Jaringan Komputer Modul 1

## Anggota:
Adrian Ismu Arifianto - 5025211116
<br>
Ahmad Rafif Hikmatiar - 5025211247

## Soal
### Soal 1

User melakukukan berbagai aktivitas menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
<br>
b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
<br>
c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
<br>
d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
<br>

**Penyelesaian**

Cara untuk mengetahui sequence number (raw) dan acknowledge number (raw) pada wireshark yaitu dengan cara memilih packet lalu di bagian bawah tekan dropdown Transmission Control Protocol. Itu dilakukan untuk menjawab semua subnomor pada soal nomor 1.

![1a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/3c6121b5-b7c3-41cd-983d-b619acc248a6)
![1b](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/fe151373-630d-4be3-a717-51e1bf41ce5c)

Berikut jawaban untuk mendapatkan flag

![terminal1](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/66e73082-1c75-44cd-ae82-b7c8712f6497)

### Soal 2

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

**Penyelesaian**

Lakukan filter di wireshark untuk mendapatkan packet yang memiliki alamat IP portal praktikum Jarkom, yaitu 10.21.78.111. Kemudian lakukan query filter dengan cara ```ip.src == 10.21.78.111```.

![2a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/12b1318d-364c-4a40-b426-862b0cba18c3)

Setelah itu, pilih salah satu packet dengan protokol HTTP, kemudian ```klik kanan -> Follow -> HTTP Stream```. Sehingga akan muncul tampilan new window dengan detail web server yang digunakan pada portal praktikum akan muncul pada bagian berikut

![2b](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/263369c6-f6e3-4e54-bf4b-20c1f05f3d38)


![2c](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/c34ccf42-435d-41ef-bf11-6aadf94d0d5f)

**Jawab:** ___Gunicorn___

### Soal 3
### Soal 4

Berapa nilai checksum yang didapat dari header pada paket nomor 130?

**Penyelesaian**

Untuk melihat nilah checksum, pertama pilih dahulu packet nomor 130 seperti yang dinyatakan dalam soal. Lalu di section bawah, pilih dropdown User Datagram Protocol dan akan tertera checksum packet tersebut

![4](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/cfbb9230-29ec-4609-9060-b829744e9a3d)

Berikut jawaban untuk mendapatkan flag

![terminal4](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/6e461858-573d-4586-8b9f-9f9f55b368fb)

### Soal 5

Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
<br>
b. Port berapakah pada server yang digunakan untuk service SMTP?
<br>
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

**Penyelesaian**

Untuk menyelesaikan soal nomor 5, pertama kita harus tahu terlebih dahulu password untuk pertanyaan flag tersebut.
<br>
1. Cari packet yang berisi password

![5a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/9af96d66-ead1-4254-a7f0-0b51a64acb12)

2. Decode password yang tertera menggunakan platform website decode online dan akan menghasilkan password asli untuk membuka file .txt yang berisi soal dari nomor 5

![5a-2](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/533e44a9-44c4-4f09-afa7-06fd4da877cc)

a. Jumlah dari packet bisa di lihat di section bawah kanan pada wireshark yang menunjukkan angka 60

![5](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/1f700c03-4773-4db8-94d8-6dc4b346d198)

b. Port dari SMTP merupakan general knowledge yang tidak berhubungan dengan wireshark jadi bisa disearch di google
<br>
c. Saya coba-coba menggunakan IP yang langsung tertera pada file pcap
<br>

Berikut jawaban untuk mendapatkan flag

![terminal5](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/5b15b021-e57c-43f9-9dd2-b47a51b64e23)

### Soal 6

Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

**Penyelesaian**

Setelah membuka file .pcap dan menemukan paket 7812, kita fokus pada pesan "SOURCE ADDRESS 7812 is invalid" dengan petunjuk bahwa "SOURCE ADDRESS ADALAH KUNCI SEMUANYA." Artinya, kita perlu melihat alamat sumber (source address) dari paket tersebut. Setelah kita melihat alamat sumber dari paket tersebut, kita menemukan bahwa alamat sumber dari paket tersebut adalah ```ip.src == 104.18.14.101```.

![6a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/39c9f82d-493b-4577-96f5-7f1d973e8b90)

Kemudian, kita menggunakan petunjuk bahwa jenis cipher yang digunakan adalah "substitusi a1z26 Cipher" dengan rentang huruf dari A-R dan jawaban yang terdiri dari 6 huruf. Jadi, kita dapat memecah alamat IP ```104.18.14.101``` menjadi 6 bagian, yaitu:

```10 4. 18. 14. 10 1```

Kemudian, kita melakukan substitusi huruf dengan angka sesuai ketentuan ```A=1```, ```B=2```, ```C=3```, ```D=4```, ```E=5```, ```F=6```, ```G=7```, ```H=8```, ```I=9```, ```J=10```, ```K=11```, ```L=12```, ```M=13```, ```N=14```, ```O=15```, ```P=16```, ```Q=17```, ```R=18```. 

Dengan mengikuti aturan ini, kita mendapatkan jawaban dari soal tersebut, yaitu ```JDRNJA```.

![6b](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/2d75d0aa-a045-418c-b384-7c554077be8e)

**Jawab:** ```JDRNJA```

### Soal 7

Berapa jumlah packet yang menuju IP 184.87.193.88?

**Penyelesaian**

Lakukan filter di wireshark untuk mendapatkan packet yang memiliki alamat IP 184.87.193.88 dengan cara kueri filter ```ip.dst == 184.87.193.88```.

![7a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/25ed776b-6f7e-47e4-8a79-d118113ab7de)

Setelah itu, hitung jumlah packet yang menuju IP 184.87.193.88

**Jawab:** ___6___

### Soal 8

Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

**Penyelesaian**

Untuk melakukan filter, berikut querynya

![8](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/965148f3-2913-4655-8850-bb96d15b390f)

Berikut jawaban untuk mendapatkan flag

![terminal8](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/89500557/a90f1624-d032-48fe-a99b-6ac67e463c09)

### Soal 9

Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

**Penyelesaian**

Untuk mendapatkan paket yang berasal dari alamat 10.51.40.1, gunakan kueri filter  ```ip.src == 10.51.40.1```. Setelah itu, untuk mendapatkan paket yang tidak menuju ke alamat 10.39.55.34, gunakan kueri filter ```ip.dst != 10.39.55.34```. Karena keduanya merupakan kondisi yang harus terpenuhi, keduanya harus digabungkan menggunakan operator logika ```&&```. Maka dari itu, hasil filter akan menampilkan paket-paket yang berasal dari alamat ```10.51.40.1``` dan tidak menuju ke alamat ```10.39.55.34```.

![9a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/c21ce617-a84b-4205-9341-271e3bf4eb3c)

**Jawab:** ```ip.src == 10.51.40.1 && ip.dst != 10.39.55.34```


### Soal 10

Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

**Penyelesaian**

Untuk mencari kredensial user yang benar ketika mencoba login menggunakan Telnet, kita perlu menggunakan kueri ```telnet contains "Login"```. Setelah itu akan muncul packet data yang memiliki kata login.

![10a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/61642054-9f14-47bd-b198-3be7b433d252)

Untuk melihat user dan password yang benar kita perlu melakukan, ```klik kanan -> Follow -> TCP Stream```. Maka akan muncul new window seperti ini.

![10b](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/c3cc229a-2007-46e9-b7ca-7d7a2a59cbc9)

**Jawab:** dhafin:kesayangannyak0k0



