# Process notes for ai-workshops

This is where I leave notes to myself along the way. 

## Removing __MACOSX file from zip file

After compressing, do:

`zip -d your-archive.zip "__MACOSX*"`

## Seconds in the file name:

https://stackoverflow.com/questions/50099869/ffmpeg-output-images-filename-with-time-position

`ffmpeg -i source -vf fps=1,select='not(mod(t,5))' -vsync 0 -frame_pts 1 %d.jpg`
