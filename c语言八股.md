c语言八股

- 逗号运算符最后的结果是最后一位，如

```c
x =(a=2,b=3,a+b)
结果为5
```

- printf是从右向左的，例： 

```c
int arr[] = { 11,12,13,14,15 };
int *ptr = arr;
*(ptr++) += 100; 
printf("%d %d", *ptr, *(++ptr)); 
//输出13 13
```

![image-20240307133203119](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240307133203119.png)

指针常量

常量指针

const int *p

![image-20240307134104402](C:\Users\小凡\AppData\Roaming\Typora\typora-user-images\image-20240307134104402.png)







野指针：

未初始化的指针

已释放的内存

局部变量被释放



c++八股



