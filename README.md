# 2FFmpeg

Tutorials for:  
> Using the FFmpeg library in your own projects  
> Developing with the FFmpeg library


## 1. build ffmpeg
./configure --prefix=/usr/local/ffmpeg --disable-x86asm  
make  
sudo make install

## 2. build ffmpeg + x264

### environment variable
echo "export LD_LIBRARY_PATH=/usr/local/ffmpeg/lib:$LD_LIBRARY_PATH">> ~/.bashrc  
echo "export PKG_CONFIG_PATH=/usr/local/ffmpeg/lib/pkgconfig:$PKG_CONFIG_PATH">> ~/.bashrc  
source ~/.bashrc  

### x264
./configure --prefix=/usr/local/ffmpeg --enable-shared --enable-static --enable-pic  
make  
sudo make install

### ffmpeg
./configure --prefix=/usr/local/ffmpeg --enable-libx264 --enable-gpl (--extra-cflags=-I/usr/local/ffmpeg/include --extra-cxxflags=-I/usr/local/ffmpeg/include --extra-ldflags=-L/usr/local/ffmpeg/lib)  
make  
sudo make install  
/* do not need extra-cflags */

## 3. example
gcc muxing.c -o muxing `pkg-config --cflags --libs libavdevice libavformat libavfilter libavcodec libswresample libswscale libavutil` -lx264

## 4. reference
https://wiki.multimedia.cx/index.php/Category:FFmpeg_Tutorials
