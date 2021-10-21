## Perulangan menggunakan while

Format penulisan while

```bash
while [ <some test> ]
do
<commands>
done
```

**contoh**

```bash
#!/bin/bash
clear

counter=1
while [ $counter -le 10 ]
do
	echo $counter
	((counter++))
done
```

**hasilnya**

```bash
1
2
3
4
5
6
7
8
9
10
```
**Perulangan menggunakan until**

Format penulisan until

```bash
until [ <some test> ]
do
<commands>
done
```

**contoh**

```bash
#!/bin/bash
clear

counter=1
until [ $counter -gt 10 ]
do
	echo $counter
	((counter++))
done
```

**hasilnya**

```bash
1
2
3
4
5
6
7
8
9
10
```

**Perulangan menggunakan for**

Format penulisan for

```bash
for var in <list>
do
<commands>
done
```

**contoh**
```bash
#!/bin/bash
clear

distros="Debian Ubuntu RedHat Slackware"

for distro in $distros 
do
	echo $distro
done
```

**hasilnya**

```bash
Debian
Ubuntu
RedHat
Slackware
```

Contoh lain perulangan angka

```bash
#!/bin/bash
clear

for angka in {1..10};
do
   echo "angka=$angka";
done
```

**Hasilnya**
```bash
angka=1
angka=2
angka=3
angka=4
angka=5
angka=6
angka=7
angka=8
angka=9
angka=10
```

Contoh lain perulangan angka dengan jarak lompatan 3

```bash
#!/bin/bash
clear

for i in {0..13..3}
do
    echo "$i"
done
```
**hasilnya**
```bash
0
3
6
9
12
```

## Perulangan menggunkan select

Dengan menggunakan select kita dapat membuat menu.
Format penulisan select

```bash
select var in <list>
do
<commands>
done
```

**contoh**


```bash
#!/bin/bash
clear
select DRINK in tea cofee water juice apple all none
do
   case $DRINK in
      tea|cofee|water|all) 
         echo "Go to canteen"
         ;;
      juice|apple)
         echo "Available at home"
         ;;
      none) 
         break 
         ;;
      *) echo "ERROR: Invalid selection" 
         ;;
   esac
done
```

**hasilnya**

```bash
1) tea
2) cofee
3) water
4) juice
5) apple
6) all
7) none
#? 3
Go to canteen
#?
```

**contoh**

```bash
#!/bin/bash
clear

names='Goku Naruto Luffy Exit'
echo 'Pilih karakter : '
select name in $names
do
	if [ $name == 'Exit' ]
	then
		break
	fi 
	echo "Hello $name"
done
```

**hasilnya**

```bash
Pilih karakter : 
1) Goku
2) Naruto
3) Luffy
4) Exit
#? 1
Hello Goku
#? 
```


