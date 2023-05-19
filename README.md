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
![alt text](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/RAM.png)<br />
 <br />
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
**ps** merupakan "process status" yang digunakan untuk melihat informasi tentang proses yang sedang berjalan pada sistem. Sementara, **-aux** memiliki peran untuk menginstruksikan ps agar dapat menampilkan proses dari semua pengguna dalam format yang lebih terperinci.<br />
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

Untuk tampilan lebih sederhana dan mudah dibaca oleh manusia monitoring CPU juga dapat dilihat menggunakan `htop` dan `glances` yang akan dijelaskan pada bagian *Manajemen Program*
 <br />

### Hardisk
Dalam memonitoring hardisk kita dapat menggunakan:
```
df
df -h
```
![alt text](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/hardisk.png)
df (Disk Free) digunakan untuk melihat penggunaan ruang hardisk pada sistem.<br />
Penjelasan dari proses `df` yang ditampilkan:
1. Filesystem: Menampilkan nama sistem file.
2. 1K-blocks: Menampilkan ukuran total partisi dalam satuan blok 1 kilobyte.
3. Used: Menampilkan jumlah ruang disk yang digunakan dalam satuan kilobyte.
4. Available: Menampilkan jumlah ruang disk yang tersedia untuk penggunaan dalam satuan kilobyte.
5. Use%: Menampilkan persentase penggunaan ruang disk.
6. Mounted on: Menampilkan titik pemasangan (mount point) sistem file.

## Manajemen Program
### Monitor Program yang sedang Berjalan
Kita masih tetap dapat memanfaatkan `top`, `htop`, dan `glances` dalam memonitor program yang sedang berjalan, termasuk `htop` dan `glances` memiliki kemampuan interaktif yang mendukung interaksi langsung dengan menggunakan tombol-tombol pada keyboard. Kita dapat mengurutkan daftar proses dengan mengklik kolom tertentu, menghentikan proses tertentu, mengubah tampilan, dan mengelola pengaturan lainnya dengan mudah. Demikian pula dengan `top` hanya saja tidak bisa berinteraksi langsung seperti htop dan glances. Berikut tampilannya:
```
htop
```
![til](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/htop.gif)
```
glances
```
![til](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/glances.gif)
Namun dalam penggunaannya htop dan glances perlu melakukan installasi terlebih dahulu dan berbeda dengan top.
 <br />
 
### Menghentikan Program yang sedang Berjalan
Seperti yang sudah dijelaskan di atas, bahwa htop dan glances selain memiliki peran yang sama dalam memudahkan manusia untuk membaca suatu program, namun mereka juga mempermudah penggunanya untuk dapat mangkses dan berinteraksi langsung dalam melakukan berbagai hal yang sudah disediakan. Salah satunya menghentikan program yang sedang berjalan dengan langsung memilihnya dari list data program yang sedang ditampilkan, seperti yang ditampilkan di bawah ini, saya akan menghentikan program firefox dengan menekan key `F9`
![til](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/kill.gif)
Namun sebelum menggunakan yang mudah ada baiknya kita mempelajari dulu yang sebelumnya ada. Dalam terminal kita bisa menggunakan perintah
```
kill <PID>
pkill [nama program]
killall [nama program]
```
![til](https://github.com/nadqz/Praktikum-Sistem-Operasi-SO-/blob/main/dokumentasi/kill%20__.gif)

### Otomasi Perintah (ShellScript)
### Jadwal Eksekusi dengan Cron
