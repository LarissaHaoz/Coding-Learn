# 抽象类和接口

## 抽象类

* 用 abstract 关键字来修饰一个类时，这个类叫做抽象类，用 abstract 来修饰一个方法时，这个方法叫做抽象方法
* 含有抽象方法的类必须被声明为抽象类，抽象方法必须被重写
* 抽象类不能被实例化
* 抽象方法只需声明，而不需要实现

```text
  abstract class Animal {
      private String name;

      public abstract void scream();
  }

  class Dog extends Animal {

      @Override
      public void scream() {
          System.out.println("Dog scream......");
      }
  }
```

## 接口

* 接口（interface）是抽象方法和常量值的定义的集合
* 从本质上讲，接口是一种「特殊的抽象类」，这种抽象类中只包含常量和抽象方法，而没有变量和方法的实现
* 类描述对象的属性和方法，接口则包含类要实现的方法

```text
  public interface Runner {
      public static final int id = 1;

      public void start();
      public void run();
      public void stop();
  }
```

* 接口声明的属性默认为 public static final 的
* 接口中只能定义抽象方法，而且这些方法都是默认为 public 的

**同步和异步**

**接口回调**

```text
  public interface GoHomeCallback {
        void finish(String info);
  }

  public class Test {
      public static void main(String[] args) {
          Test test = new Test();
            test.goHome(new GoHomeCallback() {

              @Override
              public void finish(String info) {
                  System.out.println(info);
              }
          });

          System.out.println("Haoz eat...");
          System.out.println("Haoz sleep...");    
      }

      public void goHome(GoHomeCallback callback) {
          System.out.println("Larissa go home...");
          new Thread(new Runnable() {

              @Override
              public void run() {
                  try {
                      Thread.sleep(5000);
                  } catch (InterruptedException e) {
                      e.printStackTrace();
                  }
                  callback.finish("Larissa come back...");
              }
          }).start();        
      }
  }
```

