```
shutdown 选项　时间
```

* shutdown可以安全地关机或重启

* 常用命令

  ```
  # 默认一分钟后关机
  # shutdown
  
  #　立刻重启 
  $ shutdown -r now
  
  # 立刻关机　
  $ shutdown now
  
  # 20:25关机　
  $ shutdown 20:25
  
  # 10分钟后关机　
  $ shutdown +10
  
  # 取消之前的关机计划　
  $ shutdown -c
  ```

> * 一般对远程服务器，不要关机，而是重启

