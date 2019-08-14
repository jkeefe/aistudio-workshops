# Process notes for ai-workshops

This is where I leave notes to myself along the way. 

## Removing __MACOSX file from zip file

After compressing, do:

```
zip -d bikes_data.zip "__MACOSX*"
zip -d bikes_data.zip "*.DS_Store"
```

## Seconds in the file name:

https://stackoverflow.com/questions/50099869/ffmpeg-output-images-filename-with-time-position

```
ffmpeg -i source -vf fps=1,select='not(mod(t,5))' -vsync 0 -frame_pts 1 %d.jpg

or

ffmpeg -i source -vf fps=1 -vsync 0 -frame_pts 1 %04d.jpg
```



## Jeremy's code for listing the confusino images

```
interp = ClassificationInterpretation.from_learner(learn)
losses,idxs = interp.top_losses()

for p in learn.data.valid_ds.x.items[idxs]:
  print(p, )
```
