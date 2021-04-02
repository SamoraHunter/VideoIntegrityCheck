# VideoIntegrityCheck
Python Windows FFMPEG mass video integrity and corrupt video check

Other solutions that check just a small portion, the first few bytes or last few will miss classify videos with middle sections missing frames. 

Solution to produce thumbnails will also have high false positives. 

This is an exhaustive, compute intensive (even with GPU enhancement) solution to passively screen large numbers of video files for corruption/missing frames / partially downloaded. 

Existing libraries (that I could locate) have limited support for file extensions, notably missing is support for WMV. This solution directly uses ffmpeg which supports a huge range of formats. 

This solution could be improved by making use of the size(number of errors) reported in the log, since a small number of errors in a very large/long video may not warrent classifiying as broken/corrupt. 
