* grep 文件名
  * 搜索文件的内容
    * -n: 显示匹配行及行号
    * -v: 显示不包含匹配文本的所有行（求反）
    * -i: 忽略大小写
    * grep -nv hello 123.txt 
    * grep -ni "hello python" 123.txt 
  * 支持模式搜索（正则表达式）
    * ^a: 搜索以a开头的行
    * b$: 搜索以b结尾的行