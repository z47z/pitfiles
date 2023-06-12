bgpfuzz

需要三个参数 分别为服务端地址，服务端端口，和客户端AS号（客户端AS由服务端配置）

服务端地址，服务端端口在144，145行修改（Test.TcpClient）

客户端AS号需要修改Bgp_Open.my_as（行14）与Bgp_Open.op.op5xx（行35） (填十进制数即可)

若遇到昨天提到的Open包顺序问题 可通过对调117，120行解决

启动命令 mono Peach.exe  --debug /<path to pit file>/pits/Net/bgpfuzz.xml 


ftpfuzz

四个参数 用户名 密码 地址 端口

用户名与密码修改8，12行（替换joe与mypwd即可）

地址端口修改203 204行
启动命令 mono Peach.exe  --debug /<path to pit file>/ftpfuzz.xml 


isisfuzz

参数：客户端mac地址，客户端网卡接口名 服务端Mac地址 服务端ip地址   (area_address system_id_dst)

客户端，服务端mac地址分别在85，86行。
客户端网卡接口名修改105行。
服务端IP地址 修改52行



若net号设置为 49.0001.0020.0200.2002.00
area_address后三位设置为49 00 01（37行）
system_id_dst设置为00 20 02 00 20 02 00（73行）

