## python基础语法

### （一）[字面量](https://so.csdn.net/so/search?q=字面量&spm=1001.2101.3001.7020)

#### 1. 定义

在代码中，被写下来的固定的**值**，称之为字面量。（相当于c中常量）

#### 2. 常用的6种值的类型

![img](https://cdn.nlark.com/yuque/0/2024/png/39035788/1713342190868-1c5d00e2-c8b9-4a6c-b34c-d109269397a7.png)

#### 3.字符串

！Python中，字符串需要用双引号包围；

！被双引号包围的都是字符串

```python
666
13.14
"黑马程序员"

print( 666 )
print( 13.14 )
print( "黑马程序员" )
··
>>666
>>13.14
>>"黑马程序员"
```



### （二） 注释

#### 1.单行注释

```python
# 我是单行注释
print( "黑马程序员" )
```

规范：#号和注释内容一般建议以一个空格隔开

#### 2. [多行注释](https://so.csdn.net/so/search?q=多行注释&spm=1001.2101.3001.7020)

```python
"""
         我是多行注释    
         666
         13.14
         "黑马程序员"
"""
 
print( 666 )
print( 13.14 )
print( "黑马程序员" )
```



### （三） 变量

#### 1. 定义

程序运行时，能储存计算结果或表示值的抽象概念。

简单的说，变量就是在程序运行时，记录数据用的

变量值可变

####  2.定义格式：

​                               变量名称 = 变量的值

```python
# 定义变量
money = 5000
 
# print输出变量
print( " 钱包还有：" , money )
 
>> 钱包还有： 5000
 
# 买了东西，花费10元
money = money - 10
print( "买了冰淇淋花费10元，还剩余：" , money , "元" )
 
>>买了冰淇淋花费10元，还剩余： 4990 元
```



### （四） 数据类型

#### 1. type()语句【具有返回值】

1）语法：

type(被查看类型的数据)

2）使用方法：

```python
a = type( 666 )
print( a )
 
print( type( 13.14 ) )
 
name = "黑马程序员"
name_type = type( name )
print( name_type )
 
>> <class 'int'>
>> <class 'float'>
>> <class 'str'>
```

#### 2. 变量无类型

查看变量的类型实际上查看的是变量存储数据的类型

字符串变量：不是字符串是变量，而是变量存储了字符串



### **（五） 数据类型转换**

#### 1.  常见的转换语句

![img](https://cdn.nlark.com/yuque/0/2024/png/39035788/1713345184440-defd55f1-9e65-4277-9724-e62411056545.png)此三种语句具有返回值

```python
num_str = str( 11 )
print( type( num_str ) , num_str )
 
float_str = str( 13.14 )
print( type( float_str ) , float_str )
 
>> <class 'str'> 11
>> <class 'str'> 13.14
num = int( "11" )
print( type( num ) , num )
 
num2 = float( "13.14" )
print( type( float ) , num2 )
 
>> <class 'int'> 11
>> <class 'float'> 13.14
```



想要将字符串转换成数字，必须要求字符串内的内容都是数字

```python
num3 = int ( "黑马程序员" )
print( type( num3 ) , num3 )
 
>> ValueError: invalid literal for int() with base 10: '黑马程序员'
# ValueError：以 10 为基数的 int（） 无效文字：“hello world”
```

浮点数转整数会丢失精度

```python
# 整数 -> 浮点数
float_num = float( 11 )
print( type( float_num ) , float_num )
 
>> <class 'float'> 11.0
 
# 浮点数 -> 整数
int_num = int( 13.14 )
print( type( int_num ) , int_num )
 
>> <class 'int'> 13
```





### （六）标识符

#### 1. 定义

用户在编程时所用的一系列名字，用于给变量、类、方法等命名。

#### 2. 命名规则

内容限定（英文，中文，数字，下划线_）

数字不可开头

 大小写敏感

不可使用关键字  

####  3. 命名规范

见名知义

下划线命名法

英文字母全小写



### （七） 运算符

1. 算术运算符：+、-、*、/、//、%、**（指数）
2. 赋值运算符：=
3. 复合赋值运算符：+=、-=、*=、/=、//=、%=、**=



### （八） 字符串扩展

#### 1. 3种定义方式

1）定义形式：

① 单引号定义法：

name = '黑马程序员'

②双引号定义法：

name = "黑马程序员"

③三引号定义法：

name = """黑马程序员"""

（③：*支持换行操作，使用变量接收它，则为字符串；不使用变量接收，则为多行注释）

```python
# 单引号定义法，使用单引号进行包围
name = '黑马程序员'
print( type(name) )
 
# 双引号定义法，写法和多行注释是一样的
name = "黑马程序员"
print( type(name) )
 
# 三引号定义法，写法和多行注释是一样的
name = """
我是
黑马
程序员
"""
print( type(name) )
 
>> <class 'str'>
>> <class 'str'>
>> <class 'str'>
```
