
This is a fix to correct a video end time. 
For example if the video is 2h 30m long but the time stamp says 20min 34sec.

```bash
ffmpeg -ignore_editlist 1 -i "input.mp4" -codec copy "output.mp4"
```
