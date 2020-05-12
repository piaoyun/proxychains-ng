
博文地址：http://piaoyun.cc/1419.html

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
```bash
sudo nano /etc/proxychains.conf
```

将：
```bash
socks4 127.0.0.1 9095
```

修改改为：
```bash
socks5 127.0.0.1 1080
```

![001.png](https://images.gitee.com/uploads/images/2020/0512/144846_2890c5ee_69044.png)

# 3.接下来就对配置好了的ProxyChains-NG进行测试
在终端输入以下命令：
```bash
proxychains4 curl www.Twitter.com
```

如果看到跟下图一致的话，那就OK了～

![002.png](https://images.gitee.com/uploads/images/2020/0512/144846_0b4fc79a_69044.png)

# 4.使用方法
```bash
proxychains4 XXX
```