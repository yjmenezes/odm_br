# odm_br
Open Drone Map dataset with images and  gcp_list.txt 85MB

Canon PowerShot SX260HS focal 4.5mm wxh 4000x3000 focal ~= 2904 pixel
GSD: 2.42cm  
Flight height: 75m
EPSG:32722 WGS84 UTM 22S
QGIS x,y=0,0 uper left corner; x:right+; y:up+, down-
ODM x,y=0,0 uper left corner; x:right+; y:down+ = abs(qgis y)
GCP x,y=0,0 upper left corner;  x=col, y=row; x={0..width-1}, y={0..height-1};
#
10 images, with GPS exif tags
19 painted targets, measured with geodetic GPS

compiled ODM , sources from git 2017-04-10

1- Rescaled Pixel_X, pixel_Y to fit resized images. From 4000x3000 to 2400x1800. 
Scale factor 0.6

from this:
EPSG:32722
658528.361 7167002.098 890.636 2460.6 233.9 IMG_5349.JPG HV01
to this:
EPSG:32722
658528.361 7167002.098 890.636 1476.4 140.3 IMG_5349.JPG HV01

and then this: ODM Pixel_X, Pixel_Y must be integers
EPSG:32722
658528.361 7167002.098 890.636  1476  140  IMG_5349.JPG HV01


2- ODM image axis 0/0 upper left corner. 
Y axis grows positive downwards.

3- empty lines, wrong header can be a problem. Extra point name field is ok.

4- first line must contain EPSG

[]s
julio
2017-04-11
