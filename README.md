# Praktikum Sistem Operasi (SO)
Dokumentasi job interview mengenai sistem operasi Linux
## Monitoring Resource Komputer
### RAM
Kita dapat menggunakan perintah seperti di bawah ini untuk menunjukkan memori yang tersedia dan bagaimana cara memori telah dialokasikan dalam Kilobytes (KB).
```
free
```
Sementara perintah -m di bawah ini untuk menampilkan memori yang tersedia dalam Megabytes (MB) dan  -h dalam Gigabytes (GB).
```
free -m
free -h
```
![alt text](https://github.com/nadqz/Doc-So/blob/main/Screenshot.png?raw=true)

### CPU
Kita dapat menggunakan perintah seperti di bawah ini untuk menunjukkan service yang sedang berjalan.
```
top
```

Penjelasan dari proses yang ditampilkan:
PID – Process ID adalah nomor unik identifikasi proses.
USER – Nama pengguna yang menjalankan proses.
PR – Angka prioritas proses.
NI – Nice value, untuk modifikasi nilai prioritas.
VIRT – Jumlah Virtual Memory yang digunakan.
RES – Memory bukan jenis SWAP yang dipakai.
SHR – Besar Memory yang kemungkinan bisa dibagikan (Shared) dengan proses lain.
S – Status dari proses.
%CPU – Berapa persen proses tersebut menggunakan CPU dari total kemampuannya.
%MEM – Berapa persen proses itu memakai Memory dari total kapasitas yang ada.
TIME+ – Berapa lama proses tersebut aktif.
COMMAND – Nama proses atau program yang sedang berjalan.
### Hardisk
