# Description
Files can always be changed in a secret way. Can you find the flag? cat.jpg
# Solving
First i like to check what this file REALLY is 
```
$ file cat.jpg
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
```
So sadly it's a normal image now we gonna see the metadata of the image using exiftool
```
└─$ exiftool cat.jpg                     
ExifTool Version Number         : 12.76
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2024:04:25 13:19:39+02:00
File Access Date/Time           : 2024:04:25 13:19:39+02:00
File Inode Change Date/Time     : 2024:04:25 13:19:39+02:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
```
So we can see the flag is the value of the license
PicoCTF{cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9}
