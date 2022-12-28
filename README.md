# x264
AVC (H.264) encoder with hypertuned preset + media server intention. (in-progress)

MSVC build: CC=cl ./configure --enable-static --prefix=${PWD}/installed && make && make install

GCC build: CC=gcc ./configure --enable-static --extra-cflags="-O3 -march=native" && make && make install && strip -s /usr/local/bin/x264.exe
           (gcc build exe is dropped into /usr/local/bin/ instead of x264 source folder)
           Bundle gcc build in MSYS2 with libffms2-4.dll, liblsmash-2.dll, zlib1.dll

Compressing for very small x264 executable: Get UPX.
                                            upx -9 --ultra-brute x264.exe
