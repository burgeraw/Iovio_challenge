# Iovio Challenge

## Task 4.1

filesize: 1.9GB (1.915.176.884 bytes)
The text file is an edge list from a graph with 134.217.728 edges. 

### .zip
real time: 2m2.209s
71% savings
(in=1915176884) (out=562711360)
This means it reduced the size of the file with an average of 11.066.824 bytes per second = 11.07MB/s

### .7z
real time: 21m25.612s
76% savings
out=455021733
This means it reduced the size of the file with an average of 1.135.767 bytes per second = 1.14MB/s

### .lz
real time: 25m8.673s
76.40% saved
1915176884 in, 452044114 out.
This means it reduced the size of the file with an average of 969.814 bytes per second = 0.97MB/s

### .gz
real time: 1m25.997s
70.6% savings
out=562711389
This means it reduced the size of the file with an average of 15.726.891 bytes per second = 15.73MB/s

### .zstd
real	0m17.912s
66.54% savings
1915176884 => 640736568 bytes
This means it reduced the size of the file with an average of 71.150.084 bytes per second = 71.15MB/s

We can conclude that .zstd offers the most optimal time/compression ratio. 

