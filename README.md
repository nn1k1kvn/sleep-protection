## Overview:

When someone prevents you from sleeping :)

Source of inspiration: [sox](http://sox.sourceforge.net/sox.html)

## Description:
create 4 audio
```
arecord -f S16_LE -c1 -r22050 -t raw -d 2 | lame -r -s 22.05 -mm -b 64 - blabla1.mp3
arecord -f S16_LE -c1 -r22050 -t raw -d 2 | lame -r -s 22.05 -mm -b 64 - blabla2.mp3
arecord -f S16_LE -c1 -r22050 -t raw -d 2 | lame -r -s 22.05 -mm -b 64 - blabla3.mp3
arecord -f S16_LE -c1 -r22050 -t raw -d 2 | lame -r -s 22.05 -mm -b 64 - blabla4.mp3
```
сreate a folder
```
mkdir blabla 
```
copy
```
cp blabla1.mp3  blabla2.mp3  blabla3.mp3  blabla4.mp3  blabla
```
start
```
while true; do rec test.flac rate 32k silence 1 0.5 0.07% 1  2.0 0.1% trim 0 0 ; mplayer blabla/blabla$(shuf -i1-4 -n1).mp3 ; sleep  $(shuf -i30-70 -
n1); done
```


## Dependencies:
```
sudo apt-get install mplayer2
```


## Feedback:
- Contact: 
