# Merge Video and Audio Using FFmpeg

If youtube-dl results in separate video and audio files, use ffmpeg to
comine them.

```
ffmpeg -i videoplayback.mp4 -i videoplayback.m4a -c:v copy -c:a copy output.mp4
```
