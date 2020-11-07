## FFmpeg codec HOWTO

## encode
```
ffmpeg-4.1/doc/examples/encode_video.c
./encode_video test.h264 libx264
./encode_video test.xxx xxx
```
## decode
```
ffmpeg-4.1/doc/examples/decode_video.c
./decode_video test.h264 test.yuv
./decode_video test.yyy test.yuv
```
## play
```
ffplay -f rawvideo -video_size 352x288 test.xxx
ffplay -i test.xxx -pix_fmt yuv420p -s 352x288
ffplay test.h264
```
## ffmpeg command
```
../ffmpeg -i test.yyy -c:v xxx -y test.xxx
../ffmpeg -s 352x288 -i test.yyy -y test.xxx
```
## copyright
```
https://wiki.multimedia.cx/index.php?title=FFmpeg_codec_HOWTO
https://blog.csdn.net/dancing_night/article/details/46361031
```
