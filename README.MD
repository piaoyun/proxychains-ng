资源搬家，转自：https://github.com/rofl0r/proxychains-ng
主要是自用，方便国内用户下载
http://sourceforge.net/projects/proxychains-ng/files


# 1.安装：
```bash
git clone https://gitee.com/piaoyun/proxychains-ng
cd proxychains-ng
./configure
make && make install
cp ./src/proxychains.conf /etc/proxychains.conf
#删除目录(可不执行)
cd .. && rm -rf proxychains-ng
```


# 2.配置
`sudo nano /etc/proxychains.conf`

将：
`socks4 127.0.0.1 9095`

修改改为：
`socks5 127.0.0.1 1080`

![001.png](http://piaoyun.cc/uploads/2020/05/2253401955.png)

# 3.接下来就对配置好了的ProxyChains-NG进行测试
在终端输入以下命令：`proxychains4 curl www.Twitter.com`

如果看到跟下图一致的话，那就OK了～
![002.png](http://piaoyun.cc/uploads/2020/05/1040364498.png)
# 4.使用方法
`proxychains4 XXX`