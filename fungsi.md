## Fungsi

Fungsi merupakan blok kode yang berisi statement atau command tertentu. Dengan memecah kode dalam beberapa fungsi membuat program lebih terstruktur. Fungsi yang sudah dibuat dapat dipanggil berulang sehingga mengurangi penulisan kode yang sama berulang-ulang.

Format penulisan

```bash
function_name () {
<commands>
}
```

atau

```bash
function function_name {
<commands>
}
```
**contoh**
```bash
#!/bin/bash

function halo(){
  echo "halo dunia :)"
}

halo
halo
```
