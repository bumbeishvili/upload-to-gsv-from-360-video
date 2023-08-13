
# Labpano - errored video gpx extract sample

`exiftool -p "gpx.fmt" -ee "230529_120659815.mp4" > "230529_120659815.gpx" -api largefilesupport=1`


# Insta 360 street view upload

## Step 1. Record

Record 360 video with GPS turned on


## Step 2. Stitch

Stitch video with insta360 studio, output h265, bit rate 135 or more

## Step 3. Reencode

Reencode video with ffmpeg in order to have a 5fps video (may be 7 fps if you record video with a car)


```bash
ffmpeg -i <input file path> -filter:v fps=30 <output file path>
````
For example
```
ffmpeg -i vid.mp4 -filter:v fps=3 output.mp4
```


## Step 4. Create GPX Files using insv2gpx

## Step 5. Use ul2gsv to authenticate on google

## Step 6. Drop gpx and video files to video2gsv
