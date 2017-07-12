### 页面间通过get向php页面传参 

url:http://touber.top/index.php?name=god

?name=god 为url的query部分

```
<?php  $_SERVER["QUERY_STRING"] ?>   
 /*query string（查询字符串），如果有的话，通过它进行页面访问。*/
```  

```
<?php $_GET["name"] ?>

直接获取query string里面的值,并提前将query string转为类似数组形式,中文乱码问题貌似也不需要考虑
```  

注意:利用 $_SERVER["QUERY_STRING"] 获取query string的时候如果有中文 结果会类似这样
`fname=Runoob&age=3&author=tom&name=%E4%B8%8A%E5%B8%9D `  
%E4%B8%8A%E5%B8%9D 转为中文是 `上帝`  
在浏览器栏中  
`http://127.0.0.1/learnPHP/01.php?fname=Runoob&age=3&author=tom&name=http://127.0.0.1/learnPHP/01.php?fname=Runoob&age=3&author=tom&name=%E4%B8%8A%E5%B8%9D`

浏览器会自动将%E4%B8%8A%E5%B8%9D转为中文字符,而复制该地址时会自动转为编码格式



