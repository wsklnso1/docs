分布式部署文档 - 环境说明
--------------------------------------------------------

环境
~~~~~~~

-  系统: CentOS 7
-  NFS IP: 192.168.100.99
-  Mariadb IP: 192.168.100.10
-  Redis ip: 192.168.100.20
-  Core IP: 192.168.100.30 192.168.100.31
-  koko IP: 192.168.100.40 192.168.100.41
-  Guacamole IP: 192.168.100.50 192.168.100.51
-  Tengine IP: 192.168.100.100

安全
~~~~~~~

- ssh、telnet 协议资产的防火墙设置允许 koko 与 core 访问
- rdp、vnc 协议资产的防火墙设置允许 guacamole 与 core 访问

其他
~~~~~~~

- 最终用户都是通过 Tengine 反向代理访问
- 负载均衡模式, 七层使用 session_sticky, 四层用 least_conn
- jumpserver/data 目录需要同步
- koko 需要使用同一个 redis
