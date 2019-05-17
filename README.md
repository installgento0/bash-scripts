# bash-scripts
Some useful bash scripts.

**video-convert: (requires ffmpeg)**
Converts a video file to a chosen common video format with a profile of your choice using ffmpeg.


Usage: 

Make the script executable:
`sudo chmod +x ./video-convert`

Run the script: 
`./video-convert filename.extension`

**image-convert: (requires imagemagick)**
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

**Observations:**

The output of `ls -l /bin/sh` for my system is dash. This means that POSIX-compliant scripts will run faster than using bash (eg. Arch linux's default setting). However, scripts written for BASH that make use of ["BASHisms"](https://mywiki.wooledge.org/Bashism) (features not defined by POSIX) basically, they won't work in dash, and some other setups.

More scripts to be added soon.
