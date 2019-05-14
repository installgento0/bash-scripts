# bash-scripts
Some useful bash scripts.

**video-convert: (requires ffmpeg)***
Converts a video file to a chosen common video format with a profile of your choice using ffmpeg.


Usage: 

Make the script executable:
`sudo chmod +x ./video-convert`

Run the script: 
`./video-convert filename.extension`

**image-convert: (requires imagemagick)***
Converts an image file to a chosen common format and scales it up/down using ImageMagick.


Usage: 

Make the script executable:
`sudo chmod +x ./image-convert`

Run the script: 
`./image-convert filename.extension`

In order to make PDF convertions:

Make the following change under ImageMagick's policy file:
`sudo nano /etc/ImageMagick-6/policy.xml`
or
`sudo nano /etc/ImageMagick/policy.xml`
under 
```xml
<policy domain="coder" rights="none" pattern="PDF" />
```
change it to 
```xml
<policy domain="coder" rights="read|write" pattern="PDF" />
```

More scripts to be added soon.
