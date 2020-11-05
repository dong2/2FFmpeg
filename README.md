# 2FFmpeg

## build ffmpeg
```
export LD_LIBRARY_PATH=/home/user/ffmpeg-4.1/bin/lib:$LD_LIBRARY_PATH
export PKG_CONFIG_PATH=/home/user/ffmpeg-4.1/bin/lib/pkgconfig:$PKG_CONFIG_PATH
./configure --prefix=/home/user/ffmpeg-4.1/bin --disable-x86asm
make
make install
```
## build ffmpeg + x264
```
1. environment variable
echo "export LD_LIBRARY_PATH=/home/user/ffmpeg-4.1/bin/lib:$LD_LIBRARY_PATH">> ~/.bashrc
echo "export PKG_CONFIG_PATH=/home/user/ffmpeg-4.1/bin/lib/pkgconfig:$PKG_CONFIG_PATH">> ~/.bashrc

source ~/.bashrc

1. ffmpeg
./configure --prefix=/home/user/ffmpeg-4.1/bin --enable-shared --enable-static --enable-pic

2. x264
./configure --prefix=/home/user/ffmpeg-4.1/bin --enable-libx264 --enable-gpl --extra-cflags=-I/home/user/ffmpeg-4.1/bin/include --extra-cxxflags=-I/home/user/ffmpeg-4.1/bin/include --extra-ldflags=-L/home/user/ffmpeg-4.1/bin/lib

*** Change user to yourself ***
```

## example
gcc muxing.c -o muxing `pkg-config --cflags --libs libavdevice libavformat libavfilter libavcodec libswresample libswscale libavutil` -lx264
