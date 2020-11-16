### build
```gcc inbuf_muxing.c -o inbuf_muxing `pkg-config --cflags --libs libavdevice libavformat libavfilter libavcodec libswresample libswscale libavutil` -lx264```

### inbuf AVIOContext or File as Input Source
./inbuf_muxing

### 
参考的https://github.com/slmax2017/ffmpeg_mp4_h264_mux
