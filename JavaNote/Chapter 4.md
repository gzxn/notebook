
![](https://tcs.teambition.net/storage/312414f4f47b813d9da7232d706ab0ef448a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQxNGY0ZjQ3YjgxM2Q5ZGE3MjMyZDcwNmFiMGVmNDQ4YSJ9.Z74Xkqx42y8FzoZm2uvcPfQ67rjCIPMxy633iyWVYpA&download=image.png "")

<br>

![](https://tcs.teambition.net/storage/3124dfb809e4675874c0c433b5b86da88eb9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkZmI4MDllNDY3NTg3NGMwYzQzM2I1Yjg2ZGE4OGViOSJ9.zmkiXve316bJ2sSrL72pQrmG5-b2vVHi2gvRxooMouM&download=image.png "")


# 4.1、类与对象（核心）

- 类：是具备某些共同的特征群体，属于广义的范畴；

- 对象：是类的具体描述，实际的产物，例如：一个具体的人一定是对象；

<br>

类本身规定了对象的行为，而在类之中有两个重要的组成部分；

- 属性：是标识每一个对象的特征，每一个对象都有自己的属性内容，所谓的属性实际上就是一个变量；

- 方法：是公共的行为，表示某些固定的操作，例如：说话。

在Java之中可以使用class来定义一个类。

<br>

- 声明并实例化对象：类名称 对象名称 = new 类名称();

- 分步进行：

    - 声明对象：类名称 对象名称 = null;

    - 实例化对象：对象名称 = new 类名称();

所有的引用数据类型，如果要想进行使用，那么必须通过关键字“new”来进行内存的分配操作（开辟内存）。

<br>

但一个类产生了实例化对象之后，就可以通过如下的两种方式进行类的简单操作：

- “对象.属性”：表示要访问类之中的属性内容；

- “对象.方法()”：表示要访问类之中的方法；

<br>

栈内存与堆内存区别：

- 栈内存：每一块栈内存保存的是一块堆内存的引用地址，可以理解为堆内存的名字，在程序之中可以简单利用对象名称来理解栈内存功能；

- 堆内存：保存每一个对象的具体信息，是真正的数据体，但是堆内存必须通过关键字“new”才可以开辟内存空间，以后不管何种情况下，只要是存在有new永恒表示开辟新的堆内存空间。

<br>

## 例子1：声明对象并实例化

```java
class Person{ // 定义类，类名称首字母大写
	String name; // 定义属性，表示姓名
	int age;  // 定义属性，表示年龄
	// 此时的方法不是在主类中定义，并且不会由主方法直接调用
	public void say() {
		System.out.println("name = " + name + "\n" + "age = " + age);
	}
}

public class Ex3{
	public static void main(String[] args ) {
		// 声明并实例化对象
		Person person = new Person();
		person.name = "ask"; // 调用类之中的name属性赋值
		person.age = 33; // 调用类之中的age属性赋值
		person.say();
	}
}
```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/312567e35b849ce41adc77288c72033796ff?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU2N2UzNWI4NDljZTQxYWRjNzcyODhjNzIwMzM3OTZmZiJ9.4H7NqAIUwkZbgfKmwFpwqJboUYO4hWpO1gEx14cuOTs&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/3124caf8e93d1a02d4a82d35a637e14d6493?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjYWY4ZTkzZDFhMDJkNGE4MmQzNWE2MzdlMTRkNjQ5MyJ9.3qR5kBtAwMlZ5Ep0iz7LY8vDJCrM1FTKwg513Bfqmvg&download=image.png "")

<br>

## 例子2：声明对象，实例化对象（分步）

```java
class Person{ // 定义类，类名称首字母大写
	String name; // 定义属性，表示姓名
	int age;  // 定义属性，表示年龄
	// 此时的方法不是在主类中定义，并且不会由主方法直接调用
	public void say() {
		System.out.println("name = " + name + "\n" + "age = " + age);
	}
}

public class Ex3{
	public static void main(String[] args ) {
		Person person = null;  // 声明对象
		person = new Person();  // 实例化对象
		person.name = "ask"; // 调用类之中的name属性赋值
		person.age = 33; // 调用类之中的age属性赋值
		person.say();
	}
}
```

**运行结果同上**

<br>

**内存图：**

![](https://tcs.teambition.net/storage/31240fc9a6745737702092583d4a34fa638c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQwZmM5YTY3NDU3Mzc3MDIwOTI1ODNkNGEzNGZhNjM4YyJ9.fTFM8pP1wdstusWh8-nP1lBEJAFERh0-ahdEtV5zMIU&download=image.png "")

<br>

## 例子3：引用传递（有可能产生垃圾）

```java
class Person3{ // 定义类，类名称首字母大写
	String name; // 定义属性，表示姓名
	int age;  // 定义属性，表示年龄
	// 此时的方法不是在主类中定义，并且不会由主方法直接调用
	public void say() {
		System.out.println("name = " + name + "\n" + "age = " + age);
	}
}

public class Ex3 {
	public static void main(String[] args) {
		Person3 person1 = new Person3(); //实例化对象
		Person3 person2 = new Person3(); //实例化对象
		person1.name = "fgdfk";
		person1.age = 23;
		person2.name = "afha";
		person2.age = 34;
		person2 = person1;   //引用传递产生了垃圾，person2的堆内存为垃圾
		person2.name = "eryuiw";
		person1.say();
	}
}
```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/312504526bae65f8d7345d9b6ccbd4e04566?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUwNDUyNmJhZTY1ZjhkNzM0NWQ5YjZjY2JkNGUwNDU2NiJ9.5rE8joS30Lsbp2-mcoNngi-ur2Di4soxDS9ajqPxd4Y&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/3124f053ed9336b75f6643acc1f059280180?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRmMDUzZWQ5MzM2Yjc1ZjY2NDNhY2MxZjA1OTI4MDE4MCJ9.lHO92yqIbxhF7OAHBVXS3d6cpnW_B0rKequy4_2eWYg&download=image.png "")

<br>

### 垃圾：在java中，如果某一块堆内存空间不再有任何的栈内存所指向，那么这块堆内存空间就成为垃圾，所有的垃圾空间都要等待被GC（垃圾收集器，Garbage Collector）不定期进行回收与释放。

<br>

# 4.2、封装性

如果一个类中的属性是用private来声明的，如果想要访问该类中的属性，那么就要在该类中编写setter、getter方法来访问。

<br>

**开发原则：**

以后只要是类之中的属性不需要思考永恒都要使用private封装，封装之后的属性一定要编写setter、getter方法设置和取得。

<br>

要进行操作往往都需要编写setter、getter方法。以private String name 为例：

- setter：public void setName(String n)，所有的检查操作一定要在设置上完成；

- getter：public String getName();

<br>

### 例子：setter与getter方法

```java
class Person{ // 定义类，类名称首字母大写
	private String name; // 定义属性，表示姓名
	private int age;  // 定义属性，表示年龄
	public void setName(String n){
		name = n;
	}
	public String getName(){
		return name;
	}
	public void setAge(int a){
		age = a;
	}
	public int getAge(){
		return age;
	}
	// 此时的方法不是在主类中定义，并且不会由主方法直接调用
	public void say() {
		System.out.println("name = " + name + "\n" + "age = " + age);
	}
}

public class Ex4 {
	public static void main(String[] args){
		Person per = new Person();
		per.setName("张三"); // 通过setter间接操作属性
		per.setAge(22);     // 通过setter间接操作属性
		per.say();
	}
}
```

<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31255eda20dc70fc3c745908e4ccbe3c6080?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1ZWRhMjBkYzcwZmMzYzc0NTkwOGU0Y2NiZTNjNjA4MCJ9.sKLZTU-00rCDN6Phmmscb6qAtdowvwKcwRs-tXLGJpU&download=image.png "")

<br>

setter与getter命名规则：

- set+属性名首字母大写

- get+属性名首字母大写

<br>

# 4.3构造方法

<br>

1、一个类至少有一个无参构造方法；

2、在类之中定义的构造方法只有在使用关键字new实例化新对象的时候调用一次。

3、构造方法允许进行重载，但是构造方法重载的时候只需要注重参数的类型以及个数的不同即可，方法名永恒和类名称保持一致。

<br>

![](https://tcs.teambition.net/storage/3124f26748a0f8640b923da2fa8087b1ccd6?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRmMjY3NDhhMGY4NjQwYjkyM2RhMmZhODA4N2IxY2NkNiJ9.RnyTD5cT6ZFVluz7Sl5ge8vyn6k1oaOUq6idP0t53yI&download=image.png "")

<br>

## 注意：普通方法与构造方法的定义

- 普通方法：[public | protect | private] [返回值类型] 方法名 (参数列表) { }

- 构造方法：[public | protect | private]  类名  (参数列表) { }

<br>

**范例：**
定义构造方法

```java
class Person{ // 定义类，类名称首字母大写
	public Person(){ // 方法名称与类名称相同
		System.out.println("来自构造方法");
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Person per = null;  //声明对象
		per = new Person(); //实例化对象
	}
}
```

<br>

**运行结果：**

![](https://tcs.teambition.net/storage/3125b22209f8fa674a5eb9cd21c87d1a583f?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjViMjIyMDlmOGZhNjc0YTVlYjljZDIxYzg3ZDFhNTgzZiJ9.moQNuqtm9zIExi24nyBczMkizxY4MGJThlVpRUQOILU&download=image.png "")

<br>

**范例：**
定义有参数的构造方法

```java
class Person{ // 定义类，类名称首字母大写
	public Person(String n){ // 方法名称与类名称相同
		System.out.println("来自构造方法");
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Person per = null;  //声明对象
		per = new Person("Hello"); //实例化对象
	}
}
```

**运行结果同上。**

<br>

# 4.4、匿名对象

在之前所使用的全部都是有名对象，例如发现对象的实例化格式：

- 类名称 对象名 = new 类名称();
- 对象的名字保存在栈内存之中，而每调用对象名称的时候，实际上调用的都是堆内存的操作，所以堆内存是对象真正有用的部分，那么所谓的匿名对象就是指开辟了堆内存空间，但是没有栈内存指向的对象。

<br>

```java
class Person{ // 定义类，类名称首字母大写
	private String name; // 定义属性，表示姓名
	private int age;  // 定义属性，表示年龄
	public Person(){}
	public Person(String n,int a){
		name = n;
		age = a;
	}
	public void setName(String n){
		name = n;
	}
	public String getName(){
		return name;
	}
	public void setAge(int a){
		age = a;
	}
	public int getAge(){
		return age;
	}
	// 此时的方法不是在主类中定义，并且不会由主方法直接调用
	public void say() {
		System.out.println("name = " + name + "\n" + "age = " + age);
	}
}

public class Demo {
	public static void main(String[] args) {
		new Person("张三",20).say(); // 匿名对象
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/312530b08c318581f79959d5e2576f6a0d27?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjY0NzYwNCwiaWF0IjoxNjIyMDQyODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUzMGIwOGMzMTg1ODFmNzk5NTlkNWUyNTc2ZjZhMGQyNyJ9.YYwYyKMcSCkF-dJxyC22M7afBIrR36mw3KWgOMS23tc&download=image.png "")

<br>

- 但是由于匿名类对象不会有任何的栈内存所指向，所以只能够使用一次，一次之后就将成为垃圾，并且等待被GC释放。















