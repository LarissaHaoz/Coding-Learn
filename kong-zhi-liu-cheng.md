# 控制流程

## 条件语句

也叫分支语句 — 根据不同条件，执行不同语句

### if 语句

* if
* if ... else
* if ... else if 
* if ... else if ... else if ... else 

```text
  public static void testIf() {
      int i = 1;
      if (i == 1) {
          System.out.println("i == 1");
      } else if (i == 2) {
          System.out.println("i == 2");
      } else {
          System.out.println("i == 8");
      }
  }
```

### **switch 语句**

形式：

```text
  public static void testSwitch() {
      int i = 8;
      switch (i) {
          case 1:
              System.out.println("i == 1");
              break;
          case 2:
              System.out.println("i == 2");
              break;
          default:
              System.out.println("i == 8");
              break;
      }
   }
```

注意事项：

* 小心 case 穿透，建议使用 break 语句

## **循环语句**

多次执行某些动作

* for
* while
* do ... while 

### **for 循环语句**

| 说明 | 具体内容 |
| :--- | :--- |
| 形式 | for\(语句 1；语句 2；语句 3\) { doSomething\(\); } |
| 执行过程 | 先计算语句 1，接着执行语句2，如果语句 2 的值为 true，则执行括号内的语句，接着计算语句 3，再判断语句 2 的值，依次重复下去，直到语句 2 的值为 false |

```text
  public void testFor() {
      for (int i = 0; i < 10; i++) {
          System.out.println("i = " + i);
      }
  }
```

### **while 语句**

| 说明 | 具体内容 |
| :--- | :--- |
| 形式 | while\(逻辑表达式\) { doSomething\(\); } |
| 执行过程 | 先判断逻辑表达式的值，如果值为 true，则执行后面的语句，然后再次判断条件，并重复执行，直到逻辑表达式的值为 false |

```text
  public void testWhile() {
      int b = 0;
      while (b < 10) {
          System.out.println(b);
          b++;
      }
  }
```

### **do while**

| 说明 | 具体内容 |
| :--- | :--- |
| 形式 | do { doSomething\(\) } while\(逻辑表达式\); |
| 执行过程 | 先执行语句，再判断逻辑表达式的值，如果值为 true，再执行语句，否则结束循环 |

```text
  public void testDoWhile() {
      int i = 0;
      do {
          System.out.println(i);
          i++;
      } while (i < 10);
  }
```

