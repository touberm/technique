### 关于count查询重复数据的使用  

```  
SELECT a,b as aua FROM table GROUP BY author ORDER BY aua DESC  

查询a,b(另起名为aua) 从table数据库中  用author进行分组 根据aua排序  

```

案例:workForTDYH/investorSchool/phpcms/templates/is/page_gather.html line:33行左右