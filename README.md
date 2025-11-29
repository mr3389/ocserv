----版本Ubuntu 20.04 ----！！其他版本会有小问题！！

a. 更新系统： (用不用都可以)  
  apt-get update && apt-get upgrade -y  
b. 执行一键脚本  按 1 安装  
wget -N --no-check-certificate https://raw.githubusercontent.com/mr3389/ocserv/main/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh  
c. 证书登陆步骤:  直接cd /etc/ocserv  下载配置文件
配置文件 10.10.0.0
wget -N --no-check-certificate https://raw.githubusercontent.com/mr3389/ocserv/refs/heads/main/ocserv.conf

2. 执行 mv /etc/ocserv/ssl /etc/ocserv/CAforOC  
执行以下脚本生成证书:  
wget https://raw.githubusercontent.com/mr3389/ocserv/main/testssl.sh && chmod +x testssl.sh && bash testssl.sh gc


certmgr.msc 删除多余的证书
----------------------------
启动  
/etc/init.d/ocserv start  
停止  
/etc/init.d/ocserv stop  
重启  
/etc/init.d/ocserv restart  
查看运行状态  
/etc/init.d/ocserv status  
查看日志  
/etc/init.d/ocserv log  

