# SSL routines:ssl3_read_n:unexpected eof while reading

应该是SSL证书的问题,因为我一直用的机场是80端口,所以请求https相关资源,会出现这个问题.  
要么换端口,要么不要请求https资源.  
换一个非80端口的节点应该就可以了.
