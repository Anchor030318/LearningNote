- 全局变量系统会自动初始化；
- 局部变量必须由用户自己初始化；
### c++储存类：

**auto**：声明变量时根据初始化表达式自动推断该变量的类型（C++11开始已弃用）

**register**：用于定义存储在寄存器中而不是RAM中的局部变量，即不能对他用&运算符（因为无内存地址）(已弃用）

**static：**指示编译器在程序的生命周期内保持局部变量的存在，因此使用static修饰局部变量可以在函数调用之间保持局部变量的值；

若static作用于全局变量，会使全局变量的作用域限制在声明他的文件当中；

若作用于类的数据成员上时，会使得仅有一个该成员的副本被所有对象共享；

**extern：**跨文件引用变量和函数

**thread_local:**声明的变量仅可在其创建的线程上访问

**C++引用和指针：**

1.引用不存在空引用，引用必须连接到一块合法的内存；

2.一旦引用被初始化为一个对象，就不能被指向到另一个对象，指针可以在任何时候指向到另一个对象；

3.引用必须在创建时被初始化，指针可以在任何时候被初始化；

### C++容器 set(集合)
#### unordered_set
- 关联式容器,包含的key值唯一,不会对值进行排序;
- 增加,修改和查询具有线性复杂度;
- 存储结构为hash表
##### 头文件
```C++
#include <unordered_set>
```
##### 初始化
```C++
std::unordered_set<element type> myset;//初始化为空
myset={1,2,3,4,5};//列表初始化
vector<int> myVector={1,2,3,4,5};
unordered_set myset(myVector.begin(),myVector.end());//迭代器初始化
```
##### 常用方法:
###### 判空: ```
```C++
empty();
```
###### 大小:
```C++
size();
```
###### 修改:
- 赋值:直接用“=”
- 插入:
```C++
insert(elemtype elem);
emplace(elemtype elem);
emplace_hint(Iterator it,elemtype elem);
```
- 删除:
```C++
erase(Iterator it);
extract(Iterator it);
```
- 查找:
```C++
	count(elemtype elem);//计算unordered_set中元素出现的次数,有:1,无:0
	find(elemtype elem);//返回对应元素的迭代器
```

### C++字符串string
#### 初始化
```C++
std::string s;
```
#### 常用函数:
- **获取字符串长度**
```C++
s.length();
s.size();
```
- **在字符串尾部追加字符或字符串**
```C++
std::string str1="12334"
std::string str2="whwhw"
str1.append(str2);
str1+=str2;
```
- **在指定位置插入字符或字符串**
```C++
str.insert(int pos,string str);
```
- **删除指定位置的一段字符**
```C++
str.erase(int pos,int len);
```
- **提取子字符串**
```C++
str.substr(int begin,int len);
```
- **查找字符串(返回子字符串在原来字符串中的位置)**
```C++
str.find(string str);//自左向右
str.rfind(string str1);//自右向左
```
- **替换字符串中的内容**
```C++
str.replace(int pos,int len,string str);
```
- **判空**
```C++
bool isEmpty = str.empty();
```