# tcping.py

tcping by connect in Python

```shell-session
$ python tcping.py -h
usage: tcping.py [-h] [-V] [-n N] [-i I] [-t T] host port

positional arguments:
  host           ip or FQDN
  port           port number

options:
  -h, --help     show this help message and exit
  -V, --version  show program's version number and exit
  -n N           tcping count, 0 means infinity
  -i I           tcping interval in second
  -t T           tcping timeout in second
$
$ python tcping.py 1.1.1.1 443 -n8 -t0.5 -i0.2
# tcping by connect (tcping.py)
# ip: ['1.1.1.1'] , port: 443
# count: 8
# interval: 0.2s
# timeout: 0.5s
# C:Connection time, M:Mean, Md:Median, J:Jitter
# Time Unit: millisecond
# Mean&Median&Jitter: calc the last(max) **64** valid measures
tcping 1.1.1.1:443
[2023-12-07 19:11:07.513 tcping 1.1.1.1:443 1/1] 206.823(C)  206.823(M)  206.823(Md) 0(J)
[2023-12-07 19:11:07.932 tcping 1.1.1.1:443 2/2] 218.219(C)  212.521(M)  212.521(Md) 8.058(J)
[2023-12-07 19:11:08.353 tcping 1.1.1.1:443 3/3] 219.524(C)  214.856(M)  218.219(Md) 6.987(J)
[2023-12-07 19:11:08.758 tcping 1.1.1.1:443 4/4] 204.114(C)  212.17(M)   212.521(Md) 7.835(J)
[2023-12-07 19:11:09.148 tcping 1.1.1.1:443 5/5] 190.142(C)  207.765(M)  206.823(Md) 11.962(J)
[2023-12-07 19:11:09.546 tcping 1.1.1.1:443 6/6] 197.272(C)  206.016(M)  205.469(Md) 11.525(J)
[2023-12-07 19:11:09.967 tcping 1.1.1.1:443 7/7] 219.754(C)  207.979(M)  206.823(Md) 11.732(J)
[2023-12-07 19:11:10.366 tcping 1.1.1.1:443 8/8] 198.777(C)  206.828(M)  205.469(Md) 11.339(J)
$
$ python tcping.py bing.com 443 -n4 -t0.1 -i0.1
# tcping by connect (tcping.py)
# ip: ['204.79.197.200', '13.107.21.200'] , port: 443
# count: 4
# interval: 0.1s
# timeout: 0.1s
# C:Connection time, M:Mean, Md:Median, J:Jitter
# Time Unit: millisecond
# Mean&Median&Jitter: calc the last(max) **64** valid measures
tcping 204.79.197.200:443
[2023-12-07 19:11:33.664 tcping 204.79.197.200:443 1/1] 69.196(C)   69.196(M)   69.196(Md)  0(J)
[2023-12-07 19:11:33.830 tcping 204.79.197.200:443 2/2] 65.853(C)   67.525(M)   67.525(Md)  2.364(J)
[2023-12-07 19:11:34.005 tcping 204.79.197.200:443 3/3] 74.012(C)   69.687(M)   69.196(Md)  4.101(J)
[2023-12-07 19:11:34.169 tcping 204.79.197.200:443 4/4] 62.814(C)   67.969(M)   67.525(Md)  4.798(J)
tcping 13.107.21.200:443
[2023-12-07 19:11:34.236 tcping 13.107.21.200:443 1/1] 65.648(C)   65.648(M)   65.648(Md)  0(J)
[2023-12-07 19:11:34.375 tcping 13.107.21.200:443 2/2] 38.151(C)   51.899(M)   51.899(Md)  19.444(J)
[2023-12-07 19:11:34.541 tcping 13.107.21.200:443 3/3] 65.581(C)   56.46(M)    65.581(Md)  15.856(J)
[2023-12-07 19:11:34.679 tcping 13.107.21.200:443 4/4] 37.231(C)   51.653(M)   51.866(Md)  16.126(J)
```
