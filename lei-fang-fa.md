# 类、方法

## 类

```text
public class Person {
	private String name;
	private int age;
  
  public Person(String name, int age) {
	  this.name = name;
	  this.age = age;
  }
  
  public String getName() {
	  return name;
  }
  
  public void setName(String name) {
	  this.name = name;
  }

  public int getAge() {
      return age;
  }

  public void setAge(int age) {
	  this.age = age;
  }

}
```

* 做为某个事物的模板
* 在类以外的地方，如果想要调用某个类的属性或方法，必须获取到该类的对象

### 构造器

格式：修饰符 类名 \(参数列表\) {}

```text
  public Person(String name, int age){
      this.name = name;
      this.age = age;
  }
```

* 作用：构建出类的对象
* 可以有多个

### 重载

* 为了让方法更加灵活，且清晰易懂

```text
public Person(String name, int age) {
    this.name = name;
    this.age = age;
}
```

```text
  public Person(String name) {
      this.name = name;
  }
```

### 继承

✨ Java 中使用 extends 关键字实现类的继承机制，语法规则为：

修饰符 class ChildClass extends SuperClass {}

```text
class Dog extends Animal {}
```

* 通过继承，子类自动拥有了基类（SuperClass）的所有属性和方法
* Java 只支持单继承，不允许多继承

#### **方法的重写（override）**

* 在子类中可以根据需要对从基类继承来的方法进行重写
* 重写方法必须和被重写方法具有相同方法名称，参数列表和返回类型
* 重写方法不能使用比被重写方法更严格的访问权限

#### ✨ 多态

多态是指在「运行期间」判断所引用对象的「实际类型」，根据其实际的类型调用其相应的方法

**多态的三个条件**

* 继承
* 重写
* 父类引用指向子类对象

## 方法

用来完成特定功能的代码片段（多个语句）

### **声明格式：**

修饰符 1   修饰符 2   返回值类型   方法名（形式参数列表） {       Java 语句； }

```text
public static String getName(String name) {
    return name;
}
```

* 形参（形式参数）：在方法调用时用于接收外界传入的数据
* 实参（实际参数）：调用方法时实际传给方法的数据
* 返回值：方法执行完毕后返回给调用它的环境的数据（name）

