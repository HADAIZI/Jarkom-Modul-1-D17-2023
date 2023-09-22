# Jarkom-Modul-1-D17-2023

## No. 1

![Alt text](image.png)
![Alt text](image-1.png)
![Alt text](image-2.png)

### Penjelasan Nomor 1:
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
A.  Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

Dari soal yang diberikan, kita tahu bahwa protokol yang digunakan adalah FTP dan aktivitas yang digunakan adalah mengunggah file. Karena terjadinya aktivitas upload file, maka server akan merequest dan membaca konten apa saja yang berada di file yang akan di upload, yakni melalui command STOR. Nah, maka dari itu untuk filtering-nya kita hanya perlu menggunakan 

```ftp.request.command == "STOR"```

sehingga packet yang merekam aktivitas upload file dapat dilihat sebagaimana pada gambar 1.

Karena pertanyaannya adalah berapa sequence number (raw) pada packet itu, maka kita hanya perlu membuka packet dan navigasi ke bagian Transmission Control Protocol (sebagaimana pada gambar 2) dan lihat jawabannya.

```Your answer: 258040667```

B. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?

Sama hal-nya untuk mencari acknowledge number (raw) nya yaitu dengan cara buka packet yang sama dan navigasi ke bagian Transmission Control Protocol dan nilai acknowledge number (raw) nya berada beberapa baris setelah sequence number.

```Your answer: 1044861039```

C. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Sementara itu, untuk melihat response dari aktivitas tersebut, disini saya melakukan filtering ftp dengan menggunakan nama file zip yang tadi ditemukan untuk soal a dan b, yakni GrabThePhisher. Oleh karena itu, untuk filtering kita perlu untuk menulis

```ftp.response.arg contains "GrabThePhisher"```

Sehingga kita dapat hasil packet untuk response aktivitas tersebut. Dari sini kita bisa membuka packetnya dan melihat sequence number (raw) nya dengan cara yang sama dengan soal sebelumnya.

```Your answer: 1044861039```

D. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Untuk soal D juga sama, dari hasil packet yang didapat di soal C, kita hanya perlu melihat beberapa baris dibawah sequence number (raw) dan kita mendapatkan hasil acknowledge number (raw) nya.

```
Your answer: 258040696

Correct answer!
Correct answers, you are good at addressing!
Here is your flag: Jarkom2023{y0u_r_g00d_4t_4dr3ssing_LrMwEsI60672593}
```

## No. 2

![Alt text](image-3.png)

### Penjelasan Nomor 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

Your answer: gunicorn

Correct answer!

Here is your flag: Jarkom2023{9unic0rn_1s_aH7s2eeJ7Nv690E_c00l}

## No. 3
![Alt text](image-4.png)

### Penjelasan Nomor 3

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
Your answer: 21
Correct answer!

b. Protokol layer transport apa yang digunakan?
Your answer: UDP
Correct answer!

Correct answers, you are good at analysis!
Here is your flag: Jarkom2023{4nalyz3_is_4749_RwOgSwAmPyC_gr3at}

![Alt text](image-5.png)

## No. 4
![Alt text](image-6.png)
Berapa nilai checksum yang didapat dari header pada paket nomor 130?
Your answer: 0x18e5
Correct answer!
Here is your flag: Jarkom2023{ch3cksum_is_u5eful_0xa71m}
![Alt text](image-7.png)

## No. 5
![Alt text](image-8.png)
![Alt text](image-9.png)
![Alt text](image-10.png)
![Alt text](image-11.png)
![Alt text](image-13.png)
a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
Your answer: 60
Correct answer!
![Alt text](image-12.png)
b. Port berapakah pada server yang digunakan untuk service SMTP?
Your answer: 25
Correct answer!
![Alt text](image-14.png)
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?
Your answer: 74.53.140.153
Correct answer!

## No. 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

## No. 7
![Alt text](image-15.png)
Berapa jumlah packet yang menuju IP 184.87.193.88?

Your answer: 6

Correct answer!

Here is your flag: Jarkom2023{PFAJ5oMj7rFG4013Yp_4n0th3r_f1lt3ring}

## No. 8
![Alt text](image-16.png)
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

Your answer: tcp.dstport == 80 || udp.dstport == 80

Correct answer!

## No. 9
![Alt text](image-17.png)
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

Your answer: ip.src == 10.51.40.1 && ip.dst != 10.39.55.34

Correct answer!

## No. 10
![Alt text](image-18.png)
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet, format [username]:[password]!

Your answer: dhafin:kesayangannyak0k0

Correct answer!


