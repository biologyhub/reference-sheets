# Programming quick reference

## Commands

### YouTube

```bash
# download mp4 from youtube using yt-dlp
yt-dlp -S res,ext:mp4:m4a --recode mp4 https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

### Audio

```bash
# extract audio stream without re-encoding
ffmpeg -i v.mp4 -c copy -map 0:a audio.wav

# extract first N seconds of audio from wav file
ffmpeg -ss 0 -t <N> -i audio.wav first30.wav

# resample audio
ffmpeg -i audio.wav -ar 22050 audio_22k.wav

# merge two audio channels into one
ffmpeg -i audio.wav -ac 1 audio_mono.wav

# replace audio from v.mp4 with audio from a.wav
ffmpeg -i v.mp4 -i a.wav -c:v copy -map 0:v:0 -map 1:a:0 new.mp4
````

## Links

### Fonts
- https://modernfontstacks.com/
