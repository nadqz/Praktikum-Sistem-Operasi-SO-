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
![alt text](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/RAM.png)

### CPU
Kita dapat menggunakan perintah seperti di bawah ini untuk menunjukkan service yang sedang berjalan:
```
top
```
Pada `top` kita dapat menggunakan tombol 'k' untuk mengurutkan daftar proses berdasarkan penggunaan CPU dan tombol 'q' untuk keluar dari proses CPU. <br />
<br />
![til](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/CPU.gif)

Di bagian atas tampilan merupakan informasi ringkasan tentang penggunaan CPU, termasuk persentase penggunaan CPU secara keseluruhan. Sementara di bagian bawah tampilan merupakan informasi penggunaan CPU untuk setiap masing-masing proses seperti, ID proses, pengguna yang menjalankan proses, dan informasi lainnya. Selain menggunakan `top` untuk memonitor penggunaan CPU kita juga dapat menggunakan:
```
ps -aux
```
![alt text](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/px%20-aux.png)
*ps* merupakan "process status" yang digunakan untuk melihat informasi tentang proses yang sedang berjalan pada sistem. Sementara, *-aux* memiliki peran untuk menginstruksikan ps agar dapat menampilkan proses dari semua pengguna dalam format yang lebih terperinci.<br />
Penjelasan dari proses `top` yang ditampilkan:
- PID (Process ID) = nomor unik yang diberikan kepada setiap proses oleh sistem operasi.
- USER = Nama pengguna yang menjalankan proses.
- PR = Angka prioritas proses.
- NI (Nice value) = untuk modifikasi nilai prioritas.
- VIRT (Virtual Memory) = Jumlah VIRT yang digunakan.
- RES = Memory bukan jenis SWAP yang dipakai.
- SHR = Besar Memory yang kemungkinan bisa dibagikan (Shared) dengan proses lain.
- S (Status) = status proses.
- %CPU = Presentase penggunaan CPU.
- %MEM = Presentase penggunaan memori.
- TIME+ = Waktu CPU yang digunakan.
- COMMAND = Nama proses yang sedang berjalan.<br />

Penjelasan dari proses `ps -aux` yang ditampilkan:
- VSZ (Virtual Memory) = menampilkan ukuran VSZ yang digunakan.
- RSS (Resident Set Size ) = jumlah memori fisik yang digunakan.
- TTY (Terminal) = Menampilkan terminal yang digunakan.
- STAT (Status) = berjalan (R), tertidur (S), berhenti (T), dan lainnya.
- START = waktu proses dimulai.
 <br />

### Hardisk
Dalam memonitoring hardisk kita dapat menggunakan:
```
df
df -h
```
![alt text](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/hardisk.png)
