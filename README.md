# tutorial
如何搭建auto-proxy-pool并进入线报群

## 1.主机
公网ipv4主机，或者使用内网穿透出来，方法略
> 需要注意的是，国外的主机很有可能不能提取和使用国内代理商的免费代理，建议使用国内的主机

## 2.启动auto-proxy-pool
逐行执行下面的命令（示例端口号是24769，可自行修改）
```
mkdir auto-proxy-pool
cd auto-proxy-pool
docker run --name autoProxyPool -itd -v "$(pwd)":/run/data -p 24769:8080 mzzsfy/auto-proxy-pool
```

## 3.修改配置文件  
### 下载库内的标准配置文件（推荐）  
https://raw.githubusercontent.com/randomshit699/tututorial/main/proxy.yml  
将你的提取代理API填到文件内对应位置  
然后将该文件放到`auto-proxy-pool`文件夹下  
最后重启`auto-proxy-pool`  
```
docker restart autoProxyPool
```

### 或是自行修改  
在`auto-proxy-pool`文件夹下新建`proxy.yml`文件  
参考auto-proxy-pool提供的模板`proxy.template.yml`自行修改  
**关键是配置用户名和密码认证（用户名`gdot0`，密码`wings573`）**  
![image](https://github.com/randomshit699/tututorial/assets/156558122/75981798-cfd5-4ebb-864d-9857bc377b45)


### 4.将代理池ip和端口发给我
例如：`38.47.255.116:24769`  
联系我：https://t.me/gdot0  
验证通过后会邀请你进入线报群
