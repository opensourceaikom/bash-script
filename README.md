## Variabel

Dalam bash script terdapat 3 jenis variabel:
- Environment Variable
- Positional Parameter
- User Defined Variable


## Environment Variable

Environment variable adalah variabel yang digunakan oleh shell atau system Linux untuk proses kerja, seperti variabel HOME, HOSTNAME, USERNAME, dan SHELL. Penulisan nama variabelnya menggunakan huruf kapital. Untuk melihat semua nama variabel environment ketik perintah env.

**Contoh**

```bash
#!/bin/bash

echo "Nama host : $HOSTNAME";
echo "User login : $USER";
echo "Folder home : $HOME";
echo "Desktop session : $DESKTOP_SESSION";
```

**Hasilnya**

```bash
Nama host : macOS
User login : aikom
Folder home : /home/aikom
Desktop session : gnome-fallback
```

## Positional Parameter

Positional parameter adalah variabel yang digunakan oleh shell untuk menampung argumen yang diberikan kepada shell.

**Contoh**

```bash
#!/bin/bash

echo "$1 adalah seorang mahasiswa $2 asal $3";
```

Cara menjalankannya “aikom variabel1 variabel2 variabel3”

Hasilnya
```bash
./aikom aikom linux ternate
aikom adalah seorang mahasiswa linux asal ternate
```
Pada saat script dijalankan kita juga mengirim 3 argumen, musa tersimpan di variabel $1, linux di $2, dan makassar di $3. $0 diisi dengan nama file bash script.

## User Defined Variable

User defined variable adalah variabel yang dibuat sendiri oleh programer. Cara penulisan variabel :
- Dimulai dengan huruf atau underscore (_).
- Hindari pemakaian karakter spesial seperti *,&,$.
- Nama variabel case sensitive, membedakan huruf kecil dengan huruf besar. Contoh variabel “Nama” beda dengan variabel “nama”.

**contoh** 
```bash
#!/bin/bash

hapus=`clear`;
distro="ubuntu"
total=20

echo $hapus
echo "di lab komputer ada $total pc yang menggunakan linux $distro"
```

hapus=clear menggunakan kutip terbalik sehingga isi dari variabel hapus akan dibaca sebagai perintah bash.
distro=”ubuntu” menggunakan kutip dua, isinya dibaca sebagai teks/string.
total=20 tidak menggunakan kutip, isinya dibaca sebagai angka.

**Hasilnya**

```bash
di lab komputer ada 20 pc yang menggunakan linux ubuntu
```

## Menghitung Karakter Variabel

```bash
#!/bin/bash
clear

a='distro linux ubuntu'
echo ${#a} 

b=3458623
echo ${#b}
```
**Hasilnya**
```bash
19
7
```





