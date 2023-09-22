# Jarkom-Modul-1-D19-2023
Laporan Resmi Praktikum Jaringan Komputer Modul 1

## Nama Anggota:

## Soal
### Soal 1
### Soal 2

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

**Penyelesaian**

Lakukan filter di wireshark untuk mendapatkan packet yang memiliki alamat IP portal praktikum Jarkom, yaitu 10.21.78.111. Kemudian lakukan query filter dengan cara ```ip.src == 10.21.78.111```.

![2a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/2654c34a-2a5d-4c5d-b1a3-389926bbba02)

Setelah itu, pilih salah satu packet dengan protokol HTTP, kemudian ```klik kanan -> Follow -> HTTP Stream```. Sehingga akan muncul tampilan new window dengan detail web server yang digunakan pada portal praktikum akan muncul pada bagian berikut

![2b](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/13d9ad21-dcf6-4479-affb-4d0944942714)

![2c](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/e1175b60-aae7-41be-bff2-24553cc1d11a)

**Jawab:** ___Gunicorn___

### Soal 3
### Soal 4
### Soal 5
### Soal 6
### Soal 7

Berapa jumlah packet yang menuju IP 184.87.193.88?

**Penyelesaian**

Lakukan filter di wireshark untuk mendapatkan packet yang memiliki alamat IP 184.87.193.88 dengan cara kueri filter ```ip.dst == 184.87.193.88```.

![7a](https://github.com/adrianismu/Jarkom-Modul-1-D19-2023/assets/71255346/25ed776b-6f7e-47e4-8a79-d118113ab7de)

Setelah itu, hitung jumlah packet yang menuju IP 184.87.193.88

**Jawab:** ___6___



### Soal 8
### Soal 9
### Soal 10
