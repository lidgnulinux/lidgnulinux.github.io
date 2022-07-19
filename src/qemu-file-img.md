# AGNUSTIC Episode 1

# QEMU : Boot file berekstensi ".img" pada QEMU

<br>

## Awalan

Saya ingin mencoba openbsd dan saya mengunduh file bootable-nya yang berekstensi ".img". Saya melampirkan file-nya seperti file bootable biasa yang saya pakai (berekstensi ".ISO") seperti di bawah ini :

```
$ qemu-system-x86_64 -enable-kvm \
[OPSI LAIN] \
[OPSI LAIN] \
-cdrom bootable_img.img
```

Setelah saya coba boot, ternyata tidak berhasil dan itu memang kesalahan saya. Move on dan mencari cara lain, Alhamdulillah berhasil. Berikut adalah caranya.

<br>

## Boot file berekstensi ".img" pada QEMU
 
Berikut adalah langkah-langkahnya :

1. Masuk ke direktori file img-nya.

```
$ cd /path/to/img/file.
```

<br>

2. Launch qemu dan file img dengan baris perintah di bawah ini.

```
$ qemu-system-x86_64 -enable-kvm \
[OPSI LAIN] \
[OPSI LAIN] \
drive format=raw,file=file.img
```

<br>

Segera setelah perintah di atas dijalankan, kita bisa memilih file ".img" dan boot.




Tanggal Rilis	: 19-07-2022.
