# 2FFmpeg

Tutorials for:  
  Using the FFmpeg library in your own projects  
  Developing with the FFmpeg library


## 1. build ffmpeg
export LD_LIBRARY_PATH=/home/user/ffmpeg-4.1/bin/lib:$LD_LIBRARY_PATH  
export PKG_CONFIG_PATH=/home/user/ffmpeg-4.1/bin/lib/pkgconfig:$PKG_CONFIG_PATH  
./configure --prefix=/home/user/ffmpeg-4.1/bin --disable-x86asm  
make  
make install

## 2. build ffmpeg + x264

### environment variable
echo "export LD_LIBRARY_PATH=/home/user/ffmpeg-4.1/bin/lib:$LD_LIBRARY_PATH">> ~/.bashrc  
echo "export PKG_CONFIG_PATH=/home/user/ffmpeg-4.1/bin/lib/pkgconfig:$PKG_CONFIG_PATH">> ~/.bashrc  
  
source ~/.bashrc  

### x264
./configure --prefix=/home/user/ffmpeg-4.1/bin --enable-shared --enable-static --enable-pic

### ffmpeg
./configure --prefix=/home/user/ffmpeg-4.1/bin --enable-libx264 --enable-gpl --extra-cflags=-I/home/user/ffmpeg-4.1/bin/include --extra-cxxflags=-I/home/user/ffmpeg-4.1/bin/include --extra-ldflags=-L/home/user/ffmpeg-4.1/bin/lib


## 3. example
gcc muxing.c -o muxing `pkg-config --cflags --libs libavdevice libavformat libavfilter libavcodec libswresample libswscale libavutil` -lx264

## 4. reference
https://wiki.multimedia.cx/index.php/Category:FFmpeg_Tutorials
