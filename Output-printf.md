## Output dengan printf

Selain menggunakan echo, output bisa juga dilakukan dengan menggunakan printf seperti pada bahasa pemrograman C.

```bash
#!/bin/bash
clear

distro="Ubuntu 14.04 LTS";
angka=45;

printf "OS di laptop : t $distro n";
printf "angka = $angka n";
printf "%d decimal n" $angka;
printf "%o octal n" $angka;
printf "%.2f float n" $angka;
```

Format control

- %d untuk format integer
- %o untuk format octal
- %f untuk format float atau decimal
- %x untuk format hexadecimal

Informasi lebih lengkap baca manual printf.

## Input dengan read

Untuk membaca inputan dari user digunakan read, dengan format penulisan “read namavariabel”.

```bash
#!/bin/bash
clear

echo -n "Hi, masukkan nama anda : ";
read nama;
echo "Selamat datang $nama";
```
Inputan dari user tersimpan ke dalam variabel nama.

**Contoh lain**
```bash
#!/bin/bash
clear

echo "==LOGIN=="
read -p "Username: " user 
read -sp "Password:" pass
echo
echo "Selamat datang $user"
```
- -p, bisa menggunkan string pertanyaan tanpa perlu lagi menggunakan echo seperti contoh sebelumnya.
- -s, agar inputan tidak kelihatan seperti memasukkan password.

