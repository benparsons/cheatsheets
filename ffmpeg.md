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
