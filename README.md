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
1. Find the size of any image in a directory 
- Line to add: alias imageSize="identify -format \"%wx%h\" " 
-- Example use: imageSize filename.jpg

