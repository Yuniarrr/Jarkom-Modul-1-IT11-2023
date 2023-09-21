# Modul 1 Jarkom 2023 - IT11

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Dyas Amorita Radhwa Nashirah (5027211009)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Midyanisa Yuniar (5027211025)

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
  a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
  b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
  
  Karena yang diminta adalah protokol FTP maka lakukan filtering ftp || ftp-data
  
  ![filter1](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/adf3da8b-f0fa-41fa-84fd-153b64f79ee0)
  
  karena yang dicari adalah proses mengunggah file, maka dicari kata kunci STOR (kata kunci untuk upload file ke FTP server).
  
  ![STOR](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/a00bc328-8285-4159-a8a2-b6ac777da547)
    
  untuk mempermudah alur maka paket STOR tadi ditandai kemudian ubah urutannya sesuai timeline

  ![TIMELINE](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/26e4f27b-652d-4ef3-a9ab-49e1a12745cc)

  Sequence (raw) dan acknowledgement raw untuk aktivitas unggah file ada pada packet dengan kode STOR tadi
  
  ![adanb](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/e3a99005-9707-43ac-9020-86d238c1e443)

  c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
  d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Karena sudah diurutkan sesuai timeline, maka dapat dilihat bahwa paket yang merupakan respon dari aktivitas unggah file ada tepat dibawah paket dengan kode STOR

![respon](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/33e01444-765f-4c9d-9bee-a0a132e31c44)

maka masukkan informasi yang sudah didapat ke nc 

![flg1](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/ec31e93b-0bbf-4f5d-9ff5-4ef40663784e)


## Soal 2
 soal: Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
 Mencari nama web server yang digunakan pada website portal jaringan, caranya dengan melakukan filtering terhadap ip yang digunakan pada praktikum:

![nama_servernya](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/b784dc49-1746-4b30-8bee-8d27b2487338)

kemudian follow htp stream pada paket yang memiliki protokol HTTP

![followStream](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/7c9bd6f5-e770-4c29-8cb1-971975f9629c)

dari informasi diatas dapat dilihat informasi terkait server yang tertulis yaitu server: gunicorn.
Selanjutkan masukkan jawaban tersebut ke nc

![flg2](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/98bf7c98-4e69-4237-b920-f06f9044cb90)


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

## Soal 4
Soal:
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
  a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

  tinggal diurutkan saja jumlah paket, terlihat bahwa total keseluruhan adalah 60

  ![total](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/19e07324-a42f-4240-bb5d-10fb270f3f45)

  b. Port berapakah pada server yang digunakan untuk service SMTP?

  lakukan filtering SMTP

  ![SMTP_Filter](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/0ce0a05c-8f49-4300-8619-8fcc28ca0c18)

  kemudian klik salah satu paket dan cari port yang digunakan, jawaban: 25

  ![25](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/edc1a790-df90-4440-86eb-5b2d4b48e6cd)

  
  d. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

  Ip pribadi biasanya berupa 192.168.x.x, 10.x.x.x, atau 172.16.x.x hingga 172.31.x.x, maka cukup cari ip yang memiliki awalan angka selain diatas maka ditemukanlah ip 74.53.140.153

  ![public_IP](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/74c23a26-9ff5-435f-9883-7f66d1f99f8c)

Untuk mendapatkan kode nc pertama follow salah satu paket yang menggunakan protokol SMTP. 

![followSMTP](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/5ab6fb88-ba9a-4f3f-8fea-4b2863c8bf43)

Pada paket akan ditemukan sebuah kode yang sudah dienkripsi dengan base64. Kode tersebut digunakan untuk membuka password pada file .txt yang disematkan pada soal

![password](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/dda4e80e-d5f9-4481-aaa8-abba13bda57d)

untuk mengetahui password, dilakukan dekripsi dengan base64

![decryptBase64](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/363c8663-007c-465f-9a92-d0c681b7675f)

setelah file dibuka dengan password yang ada, maka akan diberikan kode instance untuk nc

![instance_Unlocked](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/cbc2de3d-72ae-4244-9ad6-e4c42f446f85)

masukkan jawaban yang sudah didapat ke nc

![flg5](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/27218a47-b944-45ea-ab94-524df8c729ef)


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

## Soal 10
Soal: Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

Pertama ikuti TCP stream dari network TELNET

![telnet_follow](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/7d380edc-de52-43d3-b9df-35c74d193250)

cari kredensial telnet yang berhasil

![success](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/3c29a0f7-6469-4b78-8b70-c715b4931292)

setelah itu,  cari user yang memiliki password yang sama dengan menelusuri stream sebelumnya maka ditemukan user dan passwordnya

![dhafin](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/403cf7c7-73d1-4635-8844-92e3fb6c0041)

kemudian masukkan jawaban pada nc sesuai format yang diberikan

![image](https://github.com/Yuniarrr/Jarkom-Modul-1-IT11-2023/assets/107184933/7b9668cd-0e80-4be2-b89f-23cd60d43220)


## Kesulitan

1. Kurang memahami dan mengerti bagaimana cara filtering pada wireshark
2. Perlu berpikir dua kali untuk soal - soal yang terdapat enkripsi
3. Terkecoh pada soal 10 karena rupanya perlu dicari lagi user yang sesuai dengan password yang diketahui.
