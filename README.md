# tututorial
搭建auto-proxy-pool教程

1.主机
公网ipv4或者内网穿透出来，方法略

2.启动auto-proxy-pool
逐行执行下面的命令
```
mkdir auto-proxy-pool
cd auto-proxy-pool
docker run --name autoProxyPool -itd -v "$(pwd)":/run/data -p 8080:8080 mzzsfy/auto-proxy-pool
```

3.修改配置文件
