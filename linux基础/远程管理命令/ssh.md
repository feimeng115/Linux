# SSH (secure shell)

* 可以通过ssh客户端远程登录服务器

* 数据是加密的，防止泄露

* 数据是压缩的，可以提高传输速度

* 域名

  * 是IP地址的别名，方便用户记忆

  ```
  $ ping www.baidu.com
  $ ping 183.232.231.174
  ```

* 端口号

  * 通过IP地址可以找到网络的计算机

  * 通过端口号可以找到计算机运行的应用程序

  * 常见服务端口号

    | 服务  | 端口号(默认) |
    | ----- | ------------ |
    | SSH   | 22           |
    | Web   | 80           |
    | HTTPS | 443          |
    | FTP   | 21           |



## SSH客户端的简单使用

```
ssh [-p port] user@remote
```

* user: 远程机器的用户名，如不指定就默认为当前用户

* remote: 远程机器的地址，可以是IP/域名/别名　

* port: SSH Server监听的端口号，若不指定，默认值是22

  > 使用exit退出当前用户的登录

* Windows可以下载putty或xShell



## ssh免密码登录

* 步骤1：配置公钥

  * 执行ssh-keygen即可生成，一路回车

* 步骤2：上传公钥到服务器

  * 执行ssh-copy-id -p port user@remote，即可让服务器记住我们的公钥

* 原理

  * 非对称加密算法
    * 本地使用私钥对数据进行加密/解密　
    * 服务器使用公钥对数据进行解密/加密

  > scp同样也可以使用

## ssh别名的设置

* 在~/.ssh目录下创建config文件，并添加以下内容：

```
Host ubuntu
	HostName 192.168.15.16
	User jerry
	Port 22
```



这样，就成功设置了别名，即可使用ssh ubuntu实现远程登录了，scp同样适用

