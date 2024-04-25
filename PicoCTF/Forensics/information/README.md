# Problem
## Description
Files can always be changed in a secret way. Can you find the flag? cat.jpg
## Analyse
First i like to check what this file REALLY is 
```
$ file cat.jpg
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
```
So sadly it's a normal image now we gonna see the metadata of the image using exif2tool
