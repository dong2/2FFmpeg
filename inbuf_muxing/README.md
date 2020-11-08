### build
gcc inbuf_muxing.c -o inbuf_muxing `pkg-config --cflags --libs libavdevice libavformat libavfilter libavcodec libswresample libswscale libavutil` -lx264

### inbuf AVIOContext or File as Input Source
./inbuf_muxing

### 
It's not finished yet !
