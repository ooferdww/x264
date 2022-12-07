# x264
AVC (H.264) encoder.

Build instructions:

1) Get MSYS2.
2) Get VS 2015 build tools.
3) Run MSYS2 MSYS.
4) Clone repository: git clone https://github.com/ooferdww/x264
5) Run VS2015 x64 Native Tools Command Prompt. (in start menu)
6) Navigate into MSYS2 install directory. (default: %systemdrive%\msys64 so execute cd /d %systemdrive%\msys64)
7) msys2_shell.cmd -mingw64 -use-full-path
8) Navigate into repo clone in mingw64 window, generally: cd x264
9) CC=cl ./configure --enable-static --prefix=${PWD}/installed && make && make install

If you've done everything correctly, x264.exe will be dropped into RepositoryClone/installed/bin

10) OPTIONAL -- Pack executable with upx -9 --ultra-brute x264.exe

(attempting to incorporate clang build support)
