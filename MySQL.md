MySQL

多对多 中间表

一对多 多的外键



多表查询 内连接 外连接 

![image-20240306184847055](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306184847055.png)

![image-20240306184326898](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306184326898.png)

![image-20240306184404103](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306184404103.png)

select e.name,e.age,e.job,d.name from emp e ,dept d where e.dept_id=d.id;

![image-20240306185148128](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306185148128.png)

select e.name,e.age,e.job,d.name from emp e inner join dept d on e.dept_id=d.id where e.age<30;

显示内连接和隐式内连接区别在于语法、显示的明显，隐式where



![image-20240306185606936](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306185606936.png)

select distinct d.id,d.name form emp e,dept d where e.dept_id=d.id;

![image-20240306190029898](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306190029898.png)

 select e.*,d.name from emp e left join dept.d on e.dept_id =d.id where e.age>40;



![image-20240306192049548](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306192049548.png)

select e.*, s.grade from emp e,salgrade s where e.salary>s.losal and e.salary<s.hisal;



![image-20240306202830324](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306202830324.png)

select e.* s.grade

from dept d,emp e,salary s

where e.salary between s.losay and s.hisay and e.dept_id=d.id and d.name="研发部"；

![image-20240306203222091](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306203222091.png)



select avg(e.salary)

from emp e,dept d

where d.name="研发部" and d.id=e.dept_id

![image-20240306203603068](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306203603068.png)

select * from emp where salary > ( select salary from emp where name="灭绝" )

![image-20240306203814363](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306203814363.png)

select * from emp where salary > ( select avg（salary） from emp )

![image-20240306203853659](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306203853659.png)

select * from emp e2 where e2.salary<(select avg(e1.salary) from emp e1 where e1.dept=e2.dept);

![image-20240306205911972](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306205911972.png)

select d.name ,d.id ,(select count(*) from emp e where e.dept_id=d.id) as "人数" from dept d；



![image-20240306211832627](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306211832627.png)

![image-20240306212038417](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306212038417.png)

![image-20240306212704262](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306212704262.png)

![image-20240306183325746](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306183325746.png)

![image-20240306184113245](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306184113245.png)

![image-20240306184123406](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306184123406.png)





git pull origin main --allow-unrelated-histories

https://blog.csdn.net/SweetoRm/article/details/134137053

![image-20240306222837889](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240306222837889.png)

![image-20240306224418701](assets/image-20240306224418701.png)

![image-20240306224619423](assets/image-20240306224619423.png)

![image-20240306224633127](assets/image-20240306224633127.png)

![image-20240306224833717](assets/image-20240306224833717.png)

![image-20240306231237629](assets/image-20240306231237629.png)

 

![image-20240306231642313](assets/image-20240306231642313.png)

![image-20240306232011829](assets/image-20240306232011829.png)

![image-20240306232304440](assets/image-20240306232304440.png)

上溢操作

![image-20240306232813820](assets/image-20240306232813820.png)

![image-20240306232858016](assets/image-20240306232858016.png)

块默认16k

![image-20240306233300946](assets/image-20240306233300946.png)

![image-20240306233311100](assets/image-20240306233311100.png)

![image-20240306233644000](assets/image-20240306233644000.png)

![image-20240307112520532](assets/image-20240307112520532.png)

![image-20240307112620341](assets/image-20240307112620341.png)

![image-20240307112836660](assets/image-20240307112836660.png)

![image-20240307112948617](assets/image-20240307112948617.png)

![image-20240307113549227](assets/image-20240307113549227.png)

![image-20240307115053308](assets/image-20240307115053308.png)

show index from

drip index name **on**

![image-20240307115844635](assets/image-20240307115844635.png)

  

执行频次 7个下划线

慢查询 etc/my.cnf

![image-20240307121322673](assets/image-20240307121322673.png)

 

![image-20240307122047071](assets/image-20240307122047071.png)

![image-20240307171301254](assets/image-20240307171301254.png)

![image-20240307171347466](assets/image-20240307171347466.png)

![image-20240307172251983](assets/image-20240307172251983.png)

   

![image-20240307173759476](assets/image-20240307173759476.png)

![image-20240307174057119](assets/image-20240307174057119.png)

![image-20240307174350314](assets/image-20240307174350314.png)

![image-20240307174418491](assets/image-20240307174418491.png)

![image-20240307175529423](assets/image-20240307175529423.png)

![image-20240307175540696](assets/image-20240307175540696.png)

![image-20240307180726356](assets/image-20240307180726356.png)

对username，password联合索引，覆盖索引，不会回表查询

![image-20240307180746237](assets/image-20240307180746237.png)

![image-20240307182905254](assets/image-20240307182905254.png)

![image-20240307182928674](assets/image-20240307182928674.png)

![image-20240307183206309](assets/image-20240307183206309.png)

![image-20240307200046794](assets/image-20240307200046794.png)

use index

sql优化 

![image-20240307210301931](assets/image-20240307210301931.png)

 

![image-20240307212615860](assets/image-20240307212615860.png)

![image-20240307212811898](assets/image-20240307212811898.png)

![image-20240307212825385](assets/image-20240307212825385.png)

![image-20240307214632168](assets/image-20240307214632168.png)

![](assets/image-20240307223656482.png)

group by 也可以用聚合索引
