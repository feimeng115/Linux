* ifconfig 

  ```
  # 查看网卡信息
  $ ifconfig
  
  # 查看IP地址
  $ ifconfig | grep inet
  ```

  > 127.0.0.1被称为本地回环/环回地址，一般用来测试本机网卡是否正常

  

* ping 

  ```
  # 检测目标主机是否连接正常
  $ ping IP地址
  
  # 检测本地网卡是否正常
  $ ping 127.0.0.1
  ```

  

