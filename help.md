# How to compile the sources

Check [readme.txt](https://github.com/ip7z/7zip/blob/main/DOC/readme.txt) first.

## 7zz for Windows

```pwsh
git clone https://github.com/ip7z/7zip.git
cd 7zip/CPP/7zip/Bundles/Alone2
nmake PLATFORM=x64
```

## 7zz for Linux

`7zz` and `7zzs` are provided by the official website.

If you want to compile from source and get the best performance on x64 platform, you need [uasm](https://github.com/Terraspace/UASM) or [asmc](https://github.com/nidud/asmc).

### use uasm

```sh
pacman -Syu uasm

git clone https://github.com/ip7z/7zip.git
cd 7zip/CPP/7zip/Bundles/Alone2
make -f makefile.gcc -j IS_X64=1 USE_ASM=1 MY_ASM=uasm
# to get 7zzs, add COMPL_STATIC=1
```

### use asmc

```sh
git clone https://github.com/nidud/asmc.git
cd asmc/source/asmc
make
make install

git clone https://github.com/ip7z/7zip.git
cd 7zip/CPP/7zip/Bundles/Alone2
make -j -f ../../cmpl_gcc_x64.mak
```
