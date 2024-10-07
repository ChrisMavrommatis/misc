# Restore Correct Video Time

This command corrects inaccurate timestamps in a video file. For example, if a video is 2 hours and 30 minutes long but its timestamp incorrectly shows 20 minutes and 34 seconds, the following FFmpeg command can be used to resolve the issue:

```bash
ffmpeg -ignore_editlist 1 -i "input.mp4" -codec copy "output.mp4"
```

The `-ignore_editlist 1` flag ensures that FFmpeg disregards any existing edit lists, which might cause incorrect durations or timestamps to appear. The `-codec copy` option is used to avoid re-encoding the video, preserving the original quality.

