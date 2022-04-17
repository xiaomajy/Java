# 一、基本的Dos命令

---



```bash
#切换盘符  D:  （进入d盘）
# 查看当前目录下的所有文件 dir
# 切换目录  cd /d F:  (切换到f盘)
#	cd ..  （返回上一级目录）
#	cd 目录名 （进入目录）
# 清理命令提示符屏幕  cls
#推出  exit
#查看电脑ip  ipconfig
# 鼠标右键粘贴
# ping 网址  （返回网址的ip地址）
#  md 文件夹名  （创建文件夹）
# cd>文件名   （创建文件）
# del 文件名  删除文件
# rd 文件夹名  删除文件夹

```

# 二、java 基本语法

---

## 1.注释

---

```bash
# 单行注释 //
# 多行注释 /*  */  
# 文档注释 /**   */  （现在用不到）
```

## 2.标识符（关键字）

---

![image-20220416175535395](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416175535395.png)

## 3.数据类型

---

### （1）.基本数据类型

---

![image-20220416180838661](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416180838661.png)

```bash
# 其中long类型一般在定义的数字后+L  如: long a=30L;
# float 类型一般在定义的数字后+F   如： float b=30.2F;
# String 不是一个数据类型，是一个类
# char 类型是一个字符   char c ="A"     char c="AB"(报错)
# 最好不用 float 和double 或者和float 进行比较，浮点数精度有误差（长度有限，存在四舍五入）
# 较长的数字可以用_分割 （_)不会输出   int a =100_000_000;  
# bool 类型默认值为false   boolean类型
```



### （2）. 引用数据类型

---

![image-20220416181701214](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416181701214.png)

### (3).字节

---

![image-20220416182036045](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416182036045.png)

### （4）.字符

---

![image-20220416183838728](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416183838728.png)

### （5）.转义字符

---

```bash
# \ ?	在书写连续多个问好时使用，防止他们被解析成三字母词
# \ ’	用于表示字符常量‘
# \ "	用于表示字符常量"
# \ \	用于表示一个反斜杠，防止他被解译成一个转义字符
# \ a	警告字符，表示：蜂鸣
# \ b	退格符
# \ f	换页符
# \ n	换行符
# \ r	回车符
# \ t	水平制表符
# \ v	垂直制表符
# \ ddd	三位八进制数代表一个ASCII字符（ddd是一个八进制数字）
# \ xdd	二为十六进制数代表一个ASCII字符（dd是一个十六进制数字）
```

### （6）.类型转换

---

![image-20220416185152524](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416185152524.png)

```bash
# 只有高到低才需要强制转换   如： int a; char c ; int b=c+a;(不会报错)
# 不能对布尔类型转换
# 转换时可能存在内存溢出 或者精度等问题
```

解决内存溢出：

![image-20220416190212350](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416190212350.png)

## 3.变量

---

![](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416191334884.png)

```bash
# 局部变量 位于main 中的变量，必须声明并初始化
# 实例变量 位于类和main之间的变量，从属于对象
# final  常量
```

## 4.运算符

---

![image-20220416193013228](C:\Users\administrat\AppData\Roaming\Typora\typora-user-images\image-20220416193013228.png)

### （2.）位运算

```bash
# 前置++ 值会变  后置++不会变  如:int a=0;  (a++)=0; (++a)=1 ; 加完以后a=1;
# 短路运算  a&&b&&c&&d  在第一个为假的地方就停止运算了
# & 既是位运算符又是逻辑运算符，&的两侧可以是int，也可以是boolean表达式，当&两侧是int时，要先把运算符两侧的数转化为二进制数再进行运算（两位数字作比较，若同为一，则该位上结果位1，否则位0；如：1001和1010 =1000 ；
# | 跟&相似，要先把运算符两侧的数转化为二进制数再进行运算，两位数字作比较，若有一个1或两个1，则结果位1 如：1001和1010=1011
# ^ 异或 ，要先把运算符两侧的数转化为二进制数再进行运算，两位数字作比较，若相同则为0，不同位1 如：1001和1010=0111
# ~ 取反 ，要先把运算符转化为二进制数再进行运算，对每位数字取反 0取1，1取0   如 ~001=110
# << 左移，将数字*2 ， 底层为将数字转换成为二进制后对首位进行左移， 如 1<<3 即将 0000 0001 变为 0000 1000 
# >> 右移，将数字/2 ， 左移右移直接与底层（二进制）打交道，效率极高
```

