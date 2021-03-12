# Personal Profile Site
Screen to gif
https://www.screentogif.com/ <-- just capture whatever on screen and makes it gif!

Download latest FFMPEG (currently 4.6.2)
https://ffmpeg.org/download.html <-- converting GIF to MP4

GIF TO MP4
ffmpeg -f gif -i INPUT.gif -pix_fmt yuv420p -c:v libx264 -movflags +faststart -filter:v crop='floor(in_w/2)*2:floor(in_h/2)*2' OUTPUT.mp4

MP4 TO IOS PLAYABLE MP4
ffmpeg -an -i INPUT.mp4 -vcodec libx264 -codec:a libmp3lame -qscale:a 1 -pix_fmt yuv420p -profile:v baseline -level 3 OUTPUT.mp4
