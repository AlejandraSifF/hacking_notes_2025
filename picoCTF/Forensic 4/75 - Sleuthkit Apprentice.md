#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)

## Solución
```
picoCTF{by73_5urf3r_3497ae6b}
```

wget https://artifacts.picoctf.net/c/136/disk.flag.img.gz
ls -lah disk.flag.img.gz
gzip -d disk.flag.img.gz
mmls disk.flag.img
fls disk.flag.img -o 360448 -r
icat disk.flag.img -o 360448 -r 2371
picoCTF{by73_5urf3r_3497ae6b}