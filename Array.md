
## Array

Array adalah kumpulan variabel dengan tipe sejenis

**Contoh**

```bash
#!/bin/bash
clear

distro=('Debian' 'Slackware' 'Redhat' 'Suse')

echo ${distro[*]};
echo ${distro[2]};
```

- Baris 4, deklarasi variabel array distro, memiliki 4 elemen.
- Baris 6, mencetak semua nilai indeks.
- Baris 7, mencetak nilai indeks ke-2. Indeks dimulai dari 0.

- distro[0] diisi oleh Debian
- distro[1] diisi oleh Slackware
- distro[2] diisi oleh Redhat
- distro[3] diisi oleh Suse

**Hasilnya**

```bash
Debian Slackware Redhat Suse
Debian
```
Cara lain deklarasi array dengan mengisi nilai indeks satu persatu

```bash
#!/bin/bash
clear

tipe[0]='txt'
tipe[1]='mp3'
tipe[2]='mpg'
tipe[3]='html'
tipe[4]='zip'

echo "Tipe file compress adalah ${tipe[4]}"
```

**Hasilnya**
```bash
Tipe file compress adalah zip
```








