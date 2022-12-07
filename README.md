# x264
AVC (H.264) encoder.

Build instructions: (OUTDATED, todo: update)

1) Get MSYS2.
2) Run MSYS2 MSYS.
3) pacman -Syu
4) Clone repository: git clone https://github.com/ooferdww/x264
7) C:\msys64\msys2_shell.cmd -mingw64 -use-full-path
8) Navigate into repo clone in mingw64 window, generally: cd x264
9) CC=gcc ./configure --enable-static && make && make install

If you've done everything correctly, x264.exe will be dropped into C:\msys64\usr\local\bin
Bundle libffms2-4.dll, liblsmash-2.dll, zlib1.dll

10) OPTIONAL -- Pack executable with upx -9 --ultra-brute x264.exe
