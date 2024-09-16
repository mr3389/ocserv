----版本Ubuntu 20.04 ----

a. 更新系统： (用不用都可以)  
  apt-get update && apt-get upgrade -y  
b. 执行一键脚本  按 1 安装  
wget -N --no-check-certificate https://raw.githubusercontent.com/mr3389/ocserv/main/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh  
c. 证书登陆步骤:      
1.  
配置文件 注释掉原先的 然后插入或修改成下面  
auth = "certificate"  
cert-user-oid = 2.5.4.3  
mtu = 1480  
删除欢迎代码 banner = "welcome doubi"  
2.   
先把 /etc/ocserv/ssl  下面的证书  复制到  /etc/ocserv/CAforOC  
cp -r  /etc/ocserv/ssl  /etc/ocserv/CAforOC  
 或者执行 mv /etc/ocserv/ssl /etc/ocserv/CAforOC  
执行以下脚本生成证书:  
wget https://raw.githubusercontent.com/mr3389/ocserv/main/testssl.sh && chmod +x testssl.sh && bash testssl.sh gc

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

