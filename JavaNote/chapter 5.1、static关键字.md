# 1、使用static定义属性

**观察程序：**
要求定义一个表示所有清华大学学校的学生信息。

```java
class Student{
	private String name;
	private int age;
	String school = "清华大学"; //此处为了方便，暂时不设置权限
	public Student() {}
	public Student(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public String getInfo() {
		return "姓名：" + this.name + "，年龄：" + this.age + "，学校：" + this.school;
	}
}

public class Ex2 {
	public static void main(String[] args) {
		Student stuA = new Student("张三",21);	
		Student stuB = new Student("李四",22);
		Student stuC = new Student("王五",23);
		System.out.println(stuA.getInfo());
		System.out.println(stuB.getInfo());
		System.out.println(stuC.getInfo());
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/3125fd80687bb74c5deda3ba08db24e253e5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM3ODYxOSwiaWF0IjoxNjIxNzczODE5LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVmZDgwNjg3YmI3NGM1ZGVkYTNiYTA4ZGIyNGUyNTNlNSJ9.4tzpoYuqvVN8YgRzAm8wRk8zqNDW9-wtDmrnaTvDC04&download=image.png "")

**内存图：**

![](https://tcs.teambition.net/storage/312564a97fa42932a9f091417c5c098169e5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjM3NzkxNSwiaWF0IjoxNjIxNzczMTE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU2NGE5N2ZhNDI5MzJhOWYwOTE0MTdjNWMwOTgxNjllNSJ9.pTSRRsGs9RIpVWoyWEoLEtyfL-lCHfM509Jb0zMeQrc&download=image.png "")


如果Student类产生1W个对象，则需要同时对1W个对象的school属性进行修改。将school属性作为一个公共属性，不仅节省了空间，而且易于统一维护，所以可以使用static关键字来声明school属性


**范例：**
使用static关键字修改

```java
class Student{
	private String name;
	private int age;
	static String school = "清华大学"; //此处为了方便，暂时不设置权限
	public Student() {}
	public Student(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public String getInfo() {
		return "姓名：" + this.name + "，年龄：" + this.age + "，学校：" + this.school;
	}
}

public class Ex2 {
	public static void main(String[] args) {
		Student stuA = new Student("张三",21);	
		Student stuB = new Student("李四",22);
		Student stuC = new Student("王五",23);
		stuA.school = "北京大学";
		System.out.println(stuA.getInfo());
		System.out.println(stuB.getInfo());
		System.out.println(stuC.getInfo());
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/31255b5e64d3b505634abf4acb535815ac42?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM3ODgyNSwiaWF0IjoxNjIxNzc0MDI1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1YjVlNjRkM2I1MDU2MzRhYmY0YWNiNTM1ODE1YWM0MiJ9.g1bzfSo0FiTAATQOdN0GMnkqzneI4fteysp1kq0Vts8&download=image.png "")

**内存图：**

![](https://tcs.teambition.net/storage/3125be08e3dcb463a620ad69abfc2fe5b242?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjM3NzkxNSwiaWF0IjoxNjIxNzczMTE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjViZTA4ZTNkY2I0NjNhNjIwYWQ2OWFiZmMyZmU1YjI0MiJ9.GIA4cL40UbEb17wPe4VKqaJaboonuoPLqhv4gYiwnSU&download=image.png "")


一般使用static定义的属性往往会通过类名称直接调用。

由于static存在由类名称直接调用的特点，所以static属性又被称为“类属性”。而且static属性可以在一个类没有实例化对象的时候直接进行访问。

**如：**

```java
class Student{
	private String name;
	private int age;
	static String school = "清华大学"; //此处为了方便，暂时不设置权限
	public Student() {}
	public Student(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public String getInfo() {
		return "姓名：" + this.name + "，年龄：" + this.age + "，学校：" + this.school;
	}
}

public class Ex2 {
	public static void main(String[] args) {
		System.out.println(Student.school);
		Student.school = "北京大学";
		System.out.println(Student.school);
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/3125eecdbbefe87593854b21838f8e22390c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM3OTAyNiwiaWF0IjoxNjIxNzc0MjI2LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVlZWNkYmJlZmU4NzU5Mzg1NGIyMTgzOGY4ZTIyMzkwYyJ9.KjjOc4qTB5y-cZCxZvbltBXEC3NIKMFwlYSl07mT0SA&download=image.png "")


# 2、使用static定义方法


**范例：**
观察static定义方法

```java
class Student{
	private String name;
	private int age;
	private static String school = "清华大学";
	public Student() {}
	public Student(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public static void setSchool(String sch) { // 参数名不统一
		school = sch;	// 没有加上this
	}
	public static String getSchool() {
		return school;  // 没有加上this
	}
	public String getInfo() {
		System.out.println("***" + getSchool());
		return "姓名：" + this.name + "，年龄：" + this.age + "，学校：" + this.school;
	} 
}

public class Ex1 {
	public static void main(String[] args) {
		System.out.println(Student.getSchool());
		Student.setSchool("北京大学");
		Student stu = new Student("张三",21);
		System.out.println(stu.getInfo());
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/3125e99fe127f6e1824fc1f0dacfb72a1e3b?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM4MDM0MCwiaWF0IjoxNjIxNzc1NTQwLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVlOTlmZTEyN2Y2ZTE4MjRmYzFmMGRhY2ZiNzJhMWUzYiJ9.Ktjw009wURuWXDxbuGS_0BCV4HrP08NibZT_RfmYgqs&download=image.png "")


**普通方法与static方法的限制：**

- 使用static方法只能够调用static属性和static方法，不能够调用任何的非static操作

- 使用非static方法可以调用任意的static属性或static方法。


首先static方法和非static方法调用的时机是不同的。static方法可以由类名称直接调用，那么在调用的时候可以没有实例化对象产生，而非static方法，必须在有实例化对象产生之后才可以调用（对象实例化之后会开辟堆内存空间，在堆内存空间之中要保存属性的信息）。


虽然static定义的属性和方法是在类之中定义的，但是却独立于类之外，不受类对象的控制。那么只有在一种情况下会选择定义static方法：如果一个类之中没有任何的属性存在，那么就可以考虑将所有的方法定义为static。


# 3、观察主方法（理解）

如果现在一个方法定义在主类之中，并且由主方法直接调用的话，则方法定义格式如下：

```java
public static 返回值类型 方法名称（参数列表）{
	[return [返回值];]
}
```

**范例：**
在主类里编写方法调用

**情况一：**
fun()方法有static关键字

```java
public class Ex1 {
	public static void main(String[] args) {	//主方法
		// static方法只能够调用static属性或者是static方法
		fun();  //调用static方法，直接调用
	}
	public static void fun() {
		System.out.println("Hello world");
	}
}
```


**情况二：**
fun()方法没有static关键字

```java
public class Ex1 {
	public static void main(String[] args) {	//主方法
		// static方法只能够调用static属性或者是static方法
		new Ex1().fun();  
	}
	public void fun() {
		System.out.println("Hello world");
	}
}
```


**分析：**

- public：表示权限；

- static：表示此方法可以由类名称直接调用；

- void：表示主方法是一切的开始，只要开头了，就没有回头路了；

- main()：是一个系统默认定义好的方法名称，使用Java解析类的时候默认找到此名称；

- String[] args：接收的参数。


**范例：**
接收参数

```java
public class TestDemo{
	public static void main(String[] args) {
		for(int i = 0;i<args.length;i++) {
			System.out.println(args[i] + "、");
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125ff382f6e1177197b3df7d8fc5468cc26?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjM3NzkxNSwiaWF0IjoxNjIxNzczMTE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVmZjM4MmY2ZTExNzcxOTdiM2RmN2Q4ZmM1NDY4Y2MyNiJ9.pD0w7JdqX6wt969PMGHc7HaL2BpEnzQh4hF1HYzLo_4&download=image.png "")

所有的参数在解析类的时候通过“空格“分隔：“java TestDemo 参数 参数 参数 ...”，当一个参数里存在空格时，则这个参数需要用“"”声明

![](https://tcs.teambition.net/storage/3125b69829ba0043a8cf1be7a784321e89a6?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjM3NzkxNSwiaWF0IjoxNjIxNzczMTE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjViNjk4MjliYTAwNDNhOGNmMWJlN2E3ODQzMjFlODlhNiJ9.Yjk7VQlEpXZeqvNHa2IZl0HJSoyi_Aqia5cnQCZSy2Y&download=image.png "")


# 4、static的使用（理解）

**功能一：**
作为统计记录使用

如果说现在有一个类要求可以统计出类之中产生多少个实例化对象，则可以使用static进行统计。由于每个新对象实例化的时候一定要调用构造方法，所以可以在构造方法里面增加统计操作。

```java
class Person{
	private static int count = 0; //统计个数
	public Person() {
		System.out.println("Person 对象个数：" + ++count);
	}
}

public class Ex3 {
	public static void main(String[] args){
		new Person();
		new Person();
		new Person();
		new Person();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125e4bd5a0c13a5ee16bc19e23b0da59d9c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM4MTE0NywiaWF0IjoxNjIxNzc2MzQ3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVlNGJkNWEwYzEzYTVlZTE2YmMxOWUyM2IwZGE1OWQ5YyJ9.WKnYKg0vB-HfPmCRgCi8Iui9wTa_RtAw1VWfPRQWo5U&download=image.png "")


**功能二：**
实现对象的自动命名

现在假设Person类里面有一个name属性，同时提供两个构造方法（无参、一个参数），通过一个参数可以由外部设置人的名字，但是如果调用的是一个无参构造，则不希望name属性的内容是null，给他一个默认的名字“无名氏 - 编号”，那么这个编号不应该重复，所以就可以使用static统计。


```java
class Person{
	private static int count = 0; // 统计个数
	private String name;
	public Person() {
		this("无名氏 - " + count++); // 自动命名
	}
	public Person(String name) {
		this.name = name;
	}
	public String getName() {
		return this.name;
	}
}

public class Ex1 {
	public static void main(String[] args) {
		System.out.println(new Person().getName());
		System.out.println(new Person("张三").getName());
		System.out.println(new Person().getName());
	}

}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31257aa7a4ca67a79de65031c35d70230847?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjM4MTYwNCwiaWF0IjoxNjIxNzc2ODA0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU3YWE3YTRjYTY3YTc5ZGU2NTAzMWMzNWQ3MDIzMDg0NyJ9.I1oEdIqMGFcsKSw16w9QMz3J5CasWL8yJjcEZDnIfLw&download=image.png "")







