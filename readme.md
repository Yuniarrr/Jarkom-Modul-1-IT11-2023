# Modul 1 Jarkom 2023 - IT11

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Dyas Amorita Radhwa Nashirah (5027211009)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Midyanisa Yuniar (5027211025)

## Soal 1

## Soal 3

Diberikan file pcap pada [link berikut](https://drive.google.com/file/d/1bYH6-AsE4H6CZ07aAUaMjiCLQH2vE6op/view?usp=drive_link)

Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702? **21**

b. Protokol layer transport apa yang digunakan? **UDP**

**ip.addr == 239.255.255.250 and udp.port == 3702**

![soal3 pcap 19_09_2023 18_45_19](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/4e124f46-0c36-4c85-b6da-08d2db52947d)

Kemudian, dimasukkan ke dalam nc

![flag soal 3](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/fe2cc114-bda8-42e2-8465-c81cccc9064a)

## Soal 4

Diberikan file pcapng pada [link berikut](https://drive.google.com/file/d/1w9q-KAs4-mmWP0xN7WBN95QTR_XFqRI1/view?usp=drive_link)

Berapa nilai checksum yang didapat dari header pada paket nomor 130? **0x18e5**

![soal4 pcap](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/86faa57c-5093-4be3-86d4-e941903087c8)

Kemudian, dimasukkan ke dalam nc

![flag soal 4](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/7d5a91ea-f355-470b-8636-534d4c0e94ed)

## Soal 7

Diberikan file pcapng pada [link berikut](https://drive.google.com/file/d/1Ufu3_1Pl9uqhuNAVE1JbxNE3zRMFrflo/view?usp=drive_link)

Berapa jumlah packet yang menuju IP 184.87.193.88? 

Dengan melakukan filtering, **ip.dst == 184.87.193.88**, sehingga didapat **6 packet**

![soal7 pcap](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/02c4ead0-080c-416c-8c92-1d51e69ed817)

Kemudian, dimasukkan ke dalam nc

![flag soal 7](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/d46a220c-d8cc-4021-a018-54402de753c4)

## Soal 8

Diberikan file pcapng pada [link berikut](https://drive.google.com/file/d/1Ufu3_1Pl9uqhuNAVE1JbxNE3zRMFrflo/view?usp=drive_link)

Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

Dengan melakukan filtering, **tcp.dstport == 80 || udp.dstport == 80**

![soal8 pcap](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/528b3da1-607e-45b2-91bf-c8bb2df3ad4c)

Kemudian, dimasukkan ke dalam nc

![flag soal 8](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/fb613ec2-60f5-48e8-a666-7b8e6aeb6c2e)

## Soal 9

Diberikan file pcapng pada [link berikut](https://drive.google.com/file/d/1Ufu3_1Pl9uqhuNAVE1JbxNE3zRMFrflo/view?usp=drive_link)

Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

Dengan melakukan filtering, **ip.src == 10.51.40.1 && ip.dst != 10.39.55.34**

![soal9 pcap](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/e977becb-2b3f-45f2-9821-e724e74b4e24)

Kemudian, dimasukkan ke dalam nc

![flag soal 9](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/88996914/d07841c9-1500-4f76-9f19-98fd74a95289)
