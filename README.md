

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
ffmpeg -i input.mp4 -filter:v fps=30 output.mp4
```

