* scp(secure copy)

  * 远程拷贝文件
  * 地址格式和ssh类似

  ```
  # 将本机当前目录的1.py文件复制到远程的home/Desktop/1.py
  scp -P port 1.py user@remote:Desktop 1.py
  
  # 将远程的home/Desktop/1.py复制到本机的当前目录下的1.py
  scp -P port　user@remote:Desktop 1.py　1.py
  
  # 将本机的aa文件夹复制到远程的home/Desktop/
  scp -P port -r aa user@remote:Desktop 
  
  # 将远程的home/Desktop/bb文件夹复制到本机当前的目录
  scp -P port -r user@remote:Desktop　bb
  ```

  

