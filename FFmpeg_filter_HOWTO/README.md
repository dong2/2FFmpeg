## FFmpeg_filter_HOWTO

```
## fliter fff example
./ffmpeg -i input.mp4 -vf fff output.mp4
```

```
 _______              ______________
|       |            |              |
| input |  demuxer   | encoded data |   decoder
| file  | ---------> | packets      | -----+
|_______|            |______________|      |
                                           v
                                       _________
                                      |         |
                                      | decoded |
                                      | frames  |
                                      |_________|
                                           |
                                           v
                                       __________
                                      |          |
                                      | filtered |
                                      | frames   |
                                      |__________|
 ________             ______________       |
|        |           |              |      |
| output | <-------- | encoded data | <----+
| file   |   muxer   | packets      |   encoder
|________|           |______________|

```

https://wiki.multimedia.cx/index.php/FFmpeg_filter_HOWTO  
https://wiki.multimedia.cx/index.php?title=Libavfilter  
https://trac.ffmpeg.org/wiki/FilteringGuide  
https://trac.ffmpeg.org/wiki/FancyFilteringExamples  
