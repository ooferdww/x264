# x264
AVC (H.264) encoder with hypertuned preset + media server intention. (in-progress)

MSVC build: CC=cl ./configure --enable-static --prefix=/usr/local && make && make install && strip -s /usr/local/bin/x264.exe

GCC build: CC=gcc ./configure --disable-lsmash --disable-audio --disable-qtaac --disable-faac --disable-mp3 --disable-lavc --enable-static --extra-cflags="-flto -O3 -march=OPTIMIZATIONSETTING -pipe -fno-plt" && make && make install && strip -s /usr/local/bin/x264.exe

OPTIMIZATIONSETTING:

generic sandybridge ivybridge haswell skylake znver1 znver2 znver3 native

Always set to native for a build that'll be used on the build machine.

Compressing for very small x264 executable:

Get UPX:
upx -9 --ultra-brute x264.exe
