# 1、内部类的基本概念

**范例：**
观察内部类的定义

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	public void fun(){
		new Inner().print(); // 创建内部类的匿名对象
	}
	class Inner{ // 内部类：在一个类中定义的类
		public void print(){ // 内部类定义的方法
			System.out.println(msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer out = new Outer();
		out.fun();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31263f951b3987d304ad30986939be5a8852?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjYzZjk1MWIzOTg3ZDMwNGFkMzA5ODY5MzliZTVhODg1MiJ9.Cnzk-eYbmgSTI4swQgF9KiDoghJp7uw3WonF_QGbWqY&download=image.png "")

<br>

如果不用内部类，并要想实现与上面同样的功能，需要考虑以下的几个问题；

1、在Inner类之中的print()方法里，如果要想输出Outer类的msg属性，那么应该首先在Outer类里定义一个getMsg()方法取得内部类的数据（private String msg）；

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	public void fun(){
		new Inner().print(); // 创建内部类的匿名对象
	}
	public String getMsg(){
		return this.msg;
	}
}
class Inner{ // 内部类：在一个类中定义的类
	public void print(){ // 内部类定义的方法
		System.out.println(new Outer().getMsg()); // 输出数据
	}
}
public class TestDemo {
	public static void main(String[] args) {
		Outer out = new Outer();
		out.fun();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126f614b9dcd25481a7da9e62bdb0c8ee97?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjZmNjE0YjlkY2QyNTQ4MWE3ZGE5ZTYyYmRiMGM4ZWU5NyJ9.X0hu0LhVANoSVLZdrV_GuMp7_JDyYuHZdq4wdjrd33U&download=image.png "")

<br>

2、如果要想在Inner类之中去调用getMsg()方法，那么必须存在有Outer类对象。那么现在就需要把out对象传递给Inner类之中。

- 如果要想操作Inner类，则必须有一个Outer类对象，所以在Inner类里面增加一个Outer类temp属性：private Outer temp;

- 在Inner类里面定义一个构造方法，通过此构造方法传递Outer类对象：public Inner(Outer temp){this.temp = temp;}

- 在print()方法里面使用temp这个Outer类对象调用getMsg()方法；

- 在Outer类实例化Inner类的时候传递当前对象（this）；

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	public void fun(){
		new Inner(this).print(); // 创建内部类的匿名对象
	}
	public String getMsg(){
		return this.msg;
	}
}
class Inner{ // 内部类：在一个类中定义的类
	private Outer temp;
	public Inner(Outer temp){
		this.temp = temp;
	}
	public void print(){ // 内部类定义的方法
		System.out.println(new Outer().getMsg()); // 输出数据
	}
}
public class TestDemo {
	public static void main(String[] args) {
		Outer out = new Outer();
		out.fun();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126b6b0187f6818d3b52d2eaa6268ccba38?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjZiNmIwMTg3ZjY4MThkM2I1MmQyZWFhNjI2OGNjYmEzOCJ9.lisQ3n0TqtiBUzxWM7iwkzkWRSGETzlBYenhBDhGJaU&download=image.png "")


- 以上操作这么麻烦，实际上只是希望完成一个类访问另一个类的私有成员，所以此时就可以发现内部类可以很方便的访问外部类之中定义的私有成员。同理，外部类可以方便访问内部类的私有成员。

<br>

**范例：**
外部类访问内部类的私有成员

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	public void fun(){
		Inner in = new Inner();
		in.print();
		System.out.println(in.num); // 访问内部类私有成员
	}
	class Inner{ // 内部类：在一个类中定义的类
		private int num = 100; // 内部类私有成员
		public void print(){ // 内部类定义的方法
			System.out.println(msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer out = new Outer();
		out.fun();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31263abfd8a7962b4247bf69143da77ef1f7?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjYzYWJmZDhhNzk2MmI0MjQ3YmY2OTE0M2RhNzdlZjFmNyJ9.SmcvADkBf_5mxLReshb5sblg50g88JgBdgPczBDLjS8&download=image.png "")

<br>

从访问属性的角度上讲，一直强调：只要是访问类之中的属性一定要加上“this”。在内部类访问外部类msg属性的时候认为应该加上“this”才算合理。如果直接使用“this.属性”，表示的是Inner类的属性，明显是错误的，所以下面应该使用“外部类.this.属性” 才表示内部类访问外部类的属性。 

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	public void fun(){
		Inner in = new Inner();
		in.print();
	}
	class Inner{ // 内部类：在一个类中定义的类
		public void print(){ // 内部类定义的方法
			System.out.println(Outer.this.msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer out = new Outer();
		out.fun();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126b9584d36dfdbfee0d35dd7edf59f0b73?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjZiOTU4NGQzNmRmZGJmZWUwZDM1ZGQ3ZWRmNTlmMGI3MyJ9.eSBpzE0sijmdB7uOVmCRiZfmwFuqXikotvAg0sxrUEM&download=image.png "")

<br>

以上的所有代码定义的内部类最终都是在Outer类之中的方法里面操作的，那么在Java里面内部类可以通过主方法直接调用。使用的语法如下：

- 外部类.内部类 内部类对象 = new 外部类().new 内部类();

<br>

在整个操作过程中可以发现，先实例化了外部类对象，而后再实例化内部类对象，因为内部类有可能访问外部类之中的属性，而所有的属性一定要在关键字new之后才会分配空间。


**范例：**
由外部操作内部类

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	class Inner{ // 内部类：在一个类中定义的类
		public void print(){ // 内部类定义的方法
			System.out.println(Outer.this.msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer.Inner in = new Outer().new Inner();
		in.print();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126144b4ef03436c7a50f8b067297dc4201?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjYxNDRiNGVmMDM0MzZjN2E1MGY4YjA2NzI5N2RjNDIwMSJ9.fssBaTvjAI8oRDXwiBFze4wWMiVo2ZiLpkC2ac7eVUE&download=image.png "")

<br>

- 现在可以发现内部类的名称是“外部类.内部类”，观察生成的*.class 文件，可以发现内部类的文件名是：“Outer$Inner.class”，在程序之中如果文件名称是“$”，那么转换到程序里面就是“.”。现在可以发现内部类的名称的确是“外部类,内部类”。

![](https://tcs.teambition.net/storage/3126e0dd16bd28bc68ad7cb36bc0cb1cbc06?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjZlMGRkMTZiZDI4YmM2OGFkN2NiMzZiYzBjYjFjYmMwNiJ9.wJoSlKjNMuOjAhxwf2EWoZnje-PF7ZJjylX7Bes6Cfc&download=image.png "")

<br>

如果说这个时候一个内部类不希望在外部类使用，那么就使用private声明内部类。

```java
class Outer{ // 外部类
	private String msg = "Hello World.";
	private class Inner{ // 内部类：在一个类中定义的类
		public void print(){ // 内部类定义的方法
			System.out.println(Outer.this.msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer.Inner in = new Outer().new Inner();
		in.print();
	}
}
```

但是，这个时候由于存在有private声明内部类，所以外部类无法使用内部类。

<br>

# 2、使用static定义内部类

如果说现在一个内部类不希望受到外部类之中属性的控制，而可以直接去实例化对象，那么在定义内部类的时候就可以使用static关键字声明，而且使用static关键字声明的内部类严格来讲就是一个外部类，只能够调用所在外部类的static属性

<br>

**范例：**
使用static定义内部类

```java
class Outer{ // 外部类
	private static String msg = "Hello World.";
	static class Inner{ // 内部类：在一个类中定义的类
		public void print(){ // 内部类定义的方法
			System.out.println(msg); // 输出数据
		}
	}
}

public class TestDemo {
	public static void main(String[] args) {
		Outer.Inner in = new Outer.Inner();
		in.print();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31262b753ff6c797b7ec204a5d46fcc654af?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjYyYjc1M2ZmNmM3OTdiN2VjMjA0YTVkNDZmY2M2NTRhZiJ9.Od5fBhErRNKpG2YKWGy4buM3veGFdRIDBBgkV36UTKk&download=image.png "")


以上例子，通过static定义的内部类，那么在主方法中创建内部类的对象格式为：

- 外部类.内部类 内部类对象 = new 外部类.内部类();

<br>

# 3、在方法中定义内部类

**范例：**
在方法中定义内部类

```java
class Outer{ // 外部类
	private static String msg = "Hello World.";
	public void fun(){ // 普通方法
		class Inner{ // 在方法里定义的内部类
			public void print(){ // 内部类定义的方法
				System.out.println(Outer.this.msg); // 输出数据
			}
		}
		new Inner().print(); // 实例化内部类对象，并调用print方法
	}
}

public class TestDemo {
	public static void main(String[] args) {
		new Outer().fun(); // 实例化内部类对象，并调用fun方法
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126094dbd060603fd4b9d9bb740ea573936?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjYwOTRkYmQwNjA2MDNmZDRiOWQ5YmI3NDBlYTU3MzkzNiJ9.hQmUKIrT-v5VxS4HXo2KPVtkfmngaoht7KEx3u9tRgM&download=image.png "")

<br>

但是在方法之中定义的内部类如果要想访问方法的参数或者是方法定义的变量，则参数或变量前应该加上一个关键字“final”（此处的final只是一个标记，并不是其真实使用）。

```java
class Outer{ // 外部类
	private static String msg = "Hello World.";
	public void fun(final int num){ // 普通方法，带final类型的参数
		class Inner{ // 在方法里定义的内部类
			public void print(){ // 内部类定义的方法
				System.out.println(Outer.this.msg); // 输出数据
				System.out.println(num);
			}
		}
		new Inner().print(); // 实例化内部类对象，并调用print方法
	}
}

public class TestDemo {
	public static void main(String[] args) {
		new Outer().fun(100); // 实例化内部类对象，并调用fun方法
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3126aeb71d84b4308b3ab6c009cac81d6697?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyNDcxMjMwOCwiaWF0IjoxNjI0MTA3NTA4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjZhZWI3MWQ4NGI0MzA4YjNhYjZjMDA5Y2FjODFkNjY5NyJ9.rJOsoTdK_Fe8-nYXQdzWvKJydCuE7OKXV75t7O3-LjI&download=image.png "")

<br>
