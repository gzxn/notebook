
# 1、普通代码块

**观察以下程序：**

```java
public class Ex1 {
	public static void main(String[] args) {
		if(true){
			int x  = 10; // 局部变量
			System.out.println("** x = " + x);
		}
		int x= 100; // 全局变量
		System.out.println("### x = " + x);
	}
}
```

<br>

**运行结果：**

![](https://tcs.teambition.net/storage/312505526ed2ae625f4b8a61a0bfc1e8034d?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjU1NTQ1NywiaWF0IjoxNjIxOTUwNjU3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUwNTUyNmVkMmFlNjI1ZjRiOGE2MWEwYmZjMWU4MDM0ZCJ9.aSICaOrQQJ5zsKxwWACMpWYnQN2JD3P3nZMskLmBmkQ&download=image.png "")

<br>

- **现在将“if(true)” 取消：**

```java
public class Ex1 {
	public static void main(String[] args) {
		{  //普通代码块
			int x  = 10; // 局部变量
			System.out.println("** x = " + x);
		}
		int x= 100; // 全局变量
		System.out.println("### x = " + x);
	}
}
```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31258db42e75de349b3be655e01288b5e56d?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjU1NTYxOSwiaWF0IjoxNjIxOTUwODE5LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU4ZGI0MmU3NWRlMzQ5YjNiZTY1NWUwMTI4OGI1ZTU2ZCJ9.vZyRIKuTbhUvO2licNFozT0BdTn4ljkizVmQoGypBUA&download=image.png "")

<br>

一般使用普通代码块是为了方便某一个方法的编写，避免变量重复的问题。

<br>

# 2、构造块

- 如果把一个代码块写在了类之中，则此代码块称为构造块。

<br>

**范例：**
观察构造代码块

<br>

```java
class Person{
	public Person() {
		System.out.println("*** Person 类的构造方法");
	}
	
	{	// 构造块
		 System.out.println("### Person 类的构造块");
	}
}

public class Ex2 {
	public static void main(String[] args){
		new Person();
		new Person();
	}
}

```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31255c04de9bd5b8511e24c9a5a99f045fe3?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjU1NjQwNCwiaWF0IjoxNjIxOTUxNjA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1YzA0ZGU5YmQ1Yjg1MTFlMjRjOWE1YTk5ZjA0NWZlMyJ9.JJSX6z46LD45KrtwjU776tsEmuV9-gF3p7BLvG8c52I&download=image.png "")

<br>

- 现在发现构造块优先于构造方法执行，而且每当有实例化对象产生的时候都要执行构造块的内容，并且会重复调用。所以，在以后的编写代码之中不要去写构造块。

<br>

# 3、静态块

静态块就是在构造块的基础上增加了**static**关键字形成的。但是静态块的使用要分两种情况，一种是定义在普通类里面，另外一种是定义在主类里面。


**范例：**
在普通类之中定义静态块。

<br>

```java
class Person{
	public Person(){
		System.out.println("*** Person类的构造方法");
	}
	{  // 构造块
		 System.out.println("### Person 类的构造块");
	}
	static { // 静态块
		System.out.println("!!! Person 类的静态块");
	}
}

public class Ex3 {
	public static void main(String[] args){
		new Person();
		new Person();
	}
}
```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31255425b3cf7fbf57c5ff0d787192ab5d35?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjU1ODg2OCwiaWF0IjoxNjIxOTU0MDY4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1NDI1YjNjZjdmYmY1N2M1ZmYwZDc4NzE5MmFiNWQzNSJ9.aPfKhlF-Xf0335puw31eRc3CArlqUcPF17BD7CqY7ys&download=image.png "")

<br>

- 可以发现静态块将优先于构造块执行，而且不管实例化多少个对象，静态块只执行一次。一般可以利用静态块为static属性初始化，但是这样并操作并不如直接为static属性在定义的时候赋值操作方便。

<br>

**范例：**
在主类之中定义静态块。

<br>

```java
public class Ex2 {
	static { // 静态块
		System.out.println("*** 静态块 ");
	}
	public static void main(String[] args) {
		System.out.println("Hello World .");
	}
}
```

<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31250f67c56d5621a137bd34fa2cbda7c5e5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjU1Nzk2MywiaWF0IjoxNjIxOTUzMTYzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUwZjY3YzU2ZDU2MjFhMTM3YmQzNGZhMmNiZGE3YzVlNSJ9.tiZGsBsln4gSrCnPr0_7baQMLaUBhog5ILx4q0VPI_c&download=image.png "")

<br>

**总结：**静态块优先于主类先执行，所以在JDK1.7之前，java一直存在一个bug。在最早的版本之后Java就一直提倡，所有的程序必须通过主方法开始执行，但是由于静态块的存在，即使类之中没有主方法，也可以利用静态块来代替主方法。但是在JDK1.7之后，这个bug解决了。

<br>

# 4、同步块（以后更新）

<br>
<br>

















