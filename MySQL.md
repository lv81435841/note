MySQL

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

