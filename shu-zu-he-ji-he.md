# 数组和集合

## 数组

数组是 Java 语言中用来存储「固定大小」的同类型元素

### 数组的声明

格式：dataType\[\] datas;

```text
   int[] ages;
```

### 数组的初始化

格式：

```text
  int[] datas = {1, 2, 3, 4, 5};
  int[] datas = new int[5];
```

### 数组的访问

格式：

* data\[i\] = j;  // 赋值
* int data = datas\[i\];  // 获取值

```text
  int[] ages = new int[5];
  ages[2] = 97; // 赋值
  int[] marks = {78, 89, 90};
  System.out.println(marks[2]); // 获取值
```

## Java 集合

* 相比于数组（Arrays）来说，集合类的长度可变，更加适合我们的开发需求
* Java 集合就像一个容器，可以存储任何类型的数据
* 不能直接存储基本数据类型，只能存储对应的包装类，int → Integer

### List（列表）

* List 中的元素都对应一个整数型的序号，标识其在 List 中的位置，可以根据序号存取容器中的元素
* 在 List 集合中我们常用到 ArrayList 这个类
* ArrayList 中的元素是可以重复的

#### **List 的声明和初始化**

```text
List<String> strList = new ArrayList<>();
```

#### **List 常用的方法**

```text
Object get(int index);
Object set(int index, Object element);
void add(Object element);
Object remove(int index);
int indexOf(Object o);
int lastIndexOf(Object o);
```

### **包装类**

| 基本数据类型 | 包装类 |
| :--- | :--- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| char | Character |
| boolean | Boolean |

