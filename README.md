# Image CLI Tools

As a web developer I have to manipulate images quite often.  For website performance, it is critical to serve optimized images at the correct size.  This is a collection of some of the scripts I use to eliminate some of the redundancy from my workflow.  Feel free to use these in your own workflow.  If you think they could be improved, let me know.  

## Requirements
The scripts I use 
* [ImageMagick](https://www.imagemagick.org/script/index.php)
* [Google WebP Converter Tool](https://developers.google.com/speed/webp/)

## Getting Started
If you are familar with running bash scripts, just grab a script you want and add it to your preffered folder in your $PATH.  If you are new to Bash scripting, you will need to create a folder to place your scripts. If you need a little kick start check out this [article](https://webdevstudios.com/2016/07/07/beginners-guide-writing-bash-and-shell-scripts/) by Brad Parbs. 

## The Scripts
* [imageResize](https://github.com/dvrs-brad/image-cli-tools/blob/master/imageResize) - Resizes and an image based on a give width.  The aspect ration of the image will be preserved and the height will be automatically resized proportional to the new width.
* [imageWebp](https://github.com/dvrs-brad/image-cli-tools/blob/master/imageWebp) - Converts and image to Webp format at 90% quality of the original.

## Useful Aliases
The following aliases shorten some of the most useful commands from ImageMagick.  You can add these to ~/.bashrc or if using zsh ~/.zshrc
### Display size of an image
```
# ~/.bashrc or ~/.zshrc
alias imageSize="identify -format \"%wx%h\" "
# exaple use: imageSize sampleImage.jpg
```

## ImageMagick from the CLI
### Resize all images in a folder
if you know the exact size
```
mogrify -resize 600x400 *.jpg
```

```
If you know the width and want the height to scale accordingly preserving the aspect ratio
```

```
mogrify -resize 1920 *.jpg
```

```
Scale your images to a set size but preserve the aspect ratio.  Your images will scale as close as posible but maintain its aspect ratio.
```

```
mogrify -resize 600x400! *.jpg
```





  

