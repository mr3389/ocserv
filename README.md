更新系统： (用不用都可以)
  apt-get update && apt-get upgrade -y  
一键脚本，执行以后按 1 安装
wget -N --no-check-certificate https://raw.githubusercontent.com/mr3389/ocserv/main/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh
测试 第二个脚本 只创建证书
bash ocserv-ssl.sh gc
