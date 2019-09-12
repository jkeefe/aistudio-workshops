# Process notes for ai-workshops

This is where I leave notes to myself along the way. 

## Removing `__MACOSX` file from zip file

After compressing, do:

```
zip -d bikes_data.zip "__MACOSX*"
zip -d bikes_data.zip "*.DS_Store"

zip -d austin_tweet_data.zip "__MACOSX*"
zip -d austin_tweet_data.zip "*.DS_Store"

```

## Seconds in the file name:

https://stackoverflow.com/questions/50099869/ffmpeg-output-images-filename-with-time-position

```
ffmpeg -i source -vf fps=1,select='not(mod(t,5))' -vsync 0 -frame_pts 1 %d.jpg

or

ffmpeg -i source -vf fps=1 -vsync 0 -frame_pts 1 %04d.jpg
```

## Jeremy's code for listing the confusing images

```
interp = ClassificationInterpretation.from_learner(learn)
losses,idxs = interp.top_losses()

for p in learn.data.valid_ds.x.items[idxs]:
  print(p, )
```

## Managing the facebook files

Jeremy's 1,700 categorizations were in JSONL format. To turn that into a csv with just the fields I wanted,
I used the command-line tool `json2csv`:

```
npm install -g json2csv
node json2csv --input only_labeled.jsonl --output ads_and_categories.csv --ndjson --fields "text","label"
```

The ads file downloaded from ProPublica was 3GB and contained 165,000 lines.

```
$ wc -l fbpac-ads-en-US.csv 
  164600 fbpac-ads-en-US.csv
```

Then took a slice:

```
tail -n 5000 fbpac-ads-en-US.csv > fbpac-ads-en-US-slice.csv
```

