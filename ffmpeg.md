# ffmpeg

## Create video from image series

`ffmpeg -start_number 1 -framerate 500 -i %06d.png -q:v 2 -r 25 -vcodec mpeg4 test.avi`

* `-start_number 1` because the default index start is 0
* `-framerate` is the number of *input* images used per second. As such it concerns the input, and must be before the `-i` arg
* `-i %06d.png` tells which files to use, `%06d` means zero-padded to 6 digits
* -q:v video quality, lower is better
* -r 25 is the *output* framerate

## convert container while retaining contents

`ffmpeg -i video.mkv -codec copy video.mp4`

## mp4 to mp3

`ffmpeg -i filename.mp4 filename.mp3`

## get file info

`ffprobe -i input.file -show_format | grep duration`

`ffprobe -i input.file -show_format`

## create video from subsection by time

`ffmpeg -i input.mov -ss 00:01:33 -c copy output.mov`

## resize

`ffmpeg -i input.jpg -vf scale=320:-1 output_320.png`