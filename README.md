# Jarkom-Modul-1-2025-K57

### Member
1. Prabaswara Febrian 5027241069
2. Erlinda Annisa Zahra 5027241108

### Reporting

## Soal 1
Dalam tahap persiapan jaringan, Eru yang berperan sebagai Router membangun dua buah Switch/Gateway sebagai penghubung utama. Switch pertama dikonfigurasi untuk terhubung dengan dua Ainur, yaitu Melkor dan Manwe, yang berfungsi sebagai client. Sementara itu, Switch kedua diarahkan untuk terhubung dengan dua Ainur lainnya, yakni Varda dan Ulmo, yang juga ditetapkan sebagai client. Dengan rancangan ini, seluruh client dapat berkomunikasi melalui router pusat sehingga alur jaringan menjadi lebih terstruktur dan sesuai dengan topologi yang telah direncanakan.
![1](images/1png)

## Soal 2
Karena pada saat itu Arda (Bumi) masih terisolasi dari dunia luar, Eru memutuskan untuk menambahkan koneksi agar dapat terhubung ke internet. Hal ini dilakukan dengan menghubungkan Router yang dijalankan oleh Eru ke jaringan eksternal sehingga seluruh entitas yang berada di dalam topologi, termasuk para Ainur sebagai client, bisa mengakses layanan internet. Dengan langkah ini, jaringan yang awalnya hanya terbatas pada komunikasi internal kini dapat berinteraksi dengan jaringan global.

## Soal 3
## Soal 4
## Soal 5
## Soal 14
      
      nc 10.15.43.32 3401

a. How many packets are recorded in the pcapng file?
Format: int

bisa dilihat di tengah pojok kanan bawah. Yang bertulis Packets: 500358.

![14a](images/14a.png)

b. What are the user that successfully logged in?
Format: user:pass

Memakai display filter 

      frame contains "Success"

lalu ada muncul 1 paket. klik kanan > follow > tcp stream.

Jawaban 

      n1enna:y4v4nn4_k3m3nt4r1
      

![14b](images/14b.png)

c. In which stream were the credentials found?
Format: int

kita bisa melihat di pojok kiri atas yang highlight berwarna hijau

Jawaban

      41824
      

![14c](images/14c.png)

d. What tools are used for brute force?
Format: Hydra v1.8.0-dev

Dengan paket yang sama seperti no a tadi. klik kanan > follow > tcp stream. lalu bisa melihat User-Agent.

Jawaban 

      Fuzz Faster U Fool v2.1.0-dev
      

![14d](images/14b.png)

## Soal 15

      nc 10.15.43.32 3402

a. What device does Melkor use?
Format: string

Kita bisa scroll kebawah hingga ada tulisan **STRING** karena disoal ada format string. Dan cari di bString yang memiliki kata.

Jawaban 

      Keyboard

![15a](images/15a.png)

b. What did Melkor write?
Format: string

kita disini memakai python3 untuk mendapatkan tulisan yang dibuat melkor. Dimana file decode_hid.py dan file pcapng jadi 1 folder. 
run di terminal: 

      python3 decode_hid.py
      

Jawaban

      UGx6X3ByMHYxZGVfeTB1cl91czNybjRtZV80bmRfcDRzc3cwcmQ=

![15b](images/15b.png)

c. What is Melkor's secret message?
Format: string

Lalu hasil dari yang dapet dari decode bisa dibacakan di website yaitu **cyberchef** dengan recipe From Base46.

Jawaban 

      Plz_pr0v1de_y0ur_us3rn4me_4nd_p4ssw0rd

![15c](images/15c.png)

## Soal 16

      nc 10.15.43.32 3403

a. What credential did the attacker use to log in?
Format: user:pass

Harus mengurutkan sesuai protocol, lalu muncul user > follow > tcp stream

Jawaban

      ind@psg420.com:{6r_6e#TfT1p

![16a](images/16a.png)

b. How many files are suspected of containing malware?
Format: int

untuk ciri ciri malware itu jenis file nya .exe

klik Follow > TCP stream, Didalam itu ada namanya q.exe,w.exe,e.exe,r.exe,t.exe

![16b](images/16b.png)

c.  What is the hash of the first file (q.exe)?
Format: sha256

Clear display filter, lalu scroll ke bawah hingga ketemu q.exe. lalu klik kanan > Follow > tcp stream. Lalu Show As diganti menjadi raw dan save. lalu buka terminal

      sha256sum nama_file

Jawaban 

      ca34b0926cdc3242bbfad1c4a0b42cc2750d90db9a272d92cfb6cb7034d2a3bd

![16c](images/16c.png)


d. What is the hash of the second file (w.exe)?
Format: sha256

lakukan hal sama seperti di C

Jawaban 

      08eb941447078ef2c6ad8d91bb2f52256c09657ecd3d5344023edccf7291e9fc

![16d](images/16d.png)

e. What is the hash of the third file (e.exe)?
Format: sha256

lakukan hal yang sama seperti di C

Jawaban 

      32e1b3732cd779af1bf7730d0ec8a7a87a084319f6a0870dc7362a15ddbd3199

![16e](images/16e.png)

f. What is the hash of the fourth file (r.exe)?
Format: sha256

lakukan hal yang sama seperti di C

Jawaban 

      4ebd58007ee933a0a8348aee2922904a7110b7fb6a316b1c7fb2c6677e613884

![16f](images/16f.png)

g. What is the hash of the fifth file (t.exe)?
Format: sha256

lakukan hal yang sama seperti di C

Jawaban

      10ce4b79180a2ddd924fdc95951d968191af2ee3b7dfc96dd6a5714dbeae613a

![16g](images/16g.png)


## Soal 17

      nc 10.15.43.32 3404

a. What is the name of the first suspicious file?
Format: file.exe

klik File > Export Objects > HTTP. Nah disini ada list listnya.

Jawaban 

      Invoice&MSO-Request.doc

![17a](images/17a.png)

Karena file .doc sering dipakai untuk menyebarkan malware lewat macro atau script berbahaya yang dieksekusi ketika dokumen dibuka.

b. What is the name of the second suspicious file?
Format: file.exe

      knr.exe

![17b](images/17a.png)

c. What is the hash of the second suspicious file (knr.exe)?
Format: sha256

Lalu save, dan membaca ke terminal 

      sha256sum nama_file
      
Jawaban 

      749e161661290e8a2d190b1a66469744127bc25bf46e5d0c6f2e835f4b92db18

![17c](images/17c.png)

## Soal 18 

      nc 10.15.43.32 3405

a. How many files are suspected of containing malware?
Format: int

untuk melihat mencurigakan file malware adalah yang memiliki file .exe

Jawaban 

      2

![18a](images/18a.png)

b.  What is the name of the first malicious file?

Melihat file pertamana yang .exe

Jawaban 

      d0p2nc6ka3f_fixhohlycj4ovqfcy_smchzo_ub83urjpphrwahjwhv_o5c0fvf6.exe

![18b](images/18a.png)

c. Apa nama file berbahaya yang kedua?

melihat file kedua yang .exe

Jawaban 

      oiku9bu68cxqenfmcsos2aek6t07_guuisgxhllixv8dx2eemqddnhyh46l8n_di.exe

![18c](images/18a.png)

d. What is the hash of the first malicious file?
Format: sha256

Bisa mendowload file pertama, lalu bisa memakai terminal:

      sha256sum nama_file
      

Jawaban 

      59896ae5f3edcb999243c7bfdc0b17eb7fe28f3a66259d797386ea470c010040

![18d](images/18d.png)
      
e. What is the hash of the second malicious file?
Format: sha256

Bisa mendowload file Kedua, lalu bisa memakai terminal:

      sha256sum nama_file


Jawaban

      cf99990bee6c378cbf56239b3cc88276eec348d82740f84e9d5c343751f82560

![18d](images/18d.png)

## Soal 19

      nc 10.15.43.32 3406

a. Who sent the threatening message?
Format: string (name)

klik protocol yang SMTP, klik kanan > follow > TCP Stream 

Jawaban

      Your Life
      

![19a](images/19a.png)

b. How much ransom did the attacker demand ($)?
Format: int

Bisa scroll kebawah hingga ketemu gambar dolar($) "To Stop me, Pay exactly 1600$ in bitcoin".

![19b](images/19b.png)

Jawaban

      1600
      

c. What is the attacker's bitcoin wallet?
Format: string

Scroll hingga ketemu text "My bitcoin wallet is: 1CWHmuF8dHt7HBGx5RKKLgg9QA2GmE3UyL"

![19c](images/19c.png)

Jawaban 

      1CWHmuF8dHt7HBGx5RKKLgg9QA2GmE3UyL


## Soal 20

      nc 10.15.43.32 3407

Langkah masukkan keylognya:
1. Edit > Preferences > protocols > pilih TLS
2. Pada opsi (Pre)-Master-Secret log filename Browse dan pilih keyslogfile.txt, lalu pencet ok.
3. Referesh

a. What encryption method is used?
Format: string

Menggunakan display Filter:

      tls.handshake.type == 2

Lalu Klik salah satu paket ServerHelllo > lihat panel tengah > expand Transport Layer Security > bagian cipher suite akan menampilkan nama. 

Jawaban 

      TLS

![20a](images/20a.png)

b. What is the name of the malicious file placed by the attacker?
Format: file.exe

Clear Display filter lalu ke File > Export objects > HTTP, lalu file dengan jenis .dll

![20b](images/20b.png)

c. What is the hash of the file containing the malware?
Format: sha256

Lalu save, dan membaca ke terminal 

      sha256sum nama_file

![20c](images/20c.png)



   
