# 3、第三个代码模型：对象比较（重点）



**范例：**观察程序代码（暂时不考虑代码意义）

```java
class Person{
	private String name;
	public Person(String name) {
		this.name = name;
	}
	public String getName() {
		return this.name;
	}
	public void change(Person per) {//接收本类对象
		per.name = "李思"; // 直接用过"对象.属性"调用
	}
}

public class Ex1 {
	public static void main(String[] args) {
		Person person = new Person("张三");
		System.out.println(person.getName());
		// person.name = "李思"; // 错误做法：name为private属性
		person.change(person);  // 正确做法
		System.out.println(person.getName());
	}
}

```



- 正常情况下如果使用了private封装，那么外部是无法通过“对象.属性”的形式操作的，但是如果现在把对象传递回了类之中。

- 那么如果说现在有两个Person类对象（name、age属性），那么如果要比较两个对象是否相等，该如何进行比较。将每一个属性分别进行比较，如果全部相同，这表示相等。



**范例：**比较两个Person类对象是否相等

**实现一：**（代码有问题：判断逻辑都在主方法）



```java
class Person{
	private String name;
	private int age;
	public Person() {}
	public Person(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public String getName() {
		return this.name;
	}
	public int getAge() {
		return this.age;
	}
}

public class Ex2 {
	public static void main(String[] args) {
		Person perA = new Person("张三",23);
		Person perB = new Person("张三",23);
		if(perA.getName().equals(perB.getName())&&perA.getAge() == perB.getAge()) {
			System.out.println("两个对象相等。");
		}else {
			System.out.println("两个对象不等。");
		}
	}
}

```



**实现二：（自定义compare方法）**



```java
class Person{
	private String name;
	private int age;
	public Person() {}
	public Person(String name,int age) {
		this.name = name;
		this.age = age;
	}
	public boolean compare(Person person) {
		if(this == person) { //地址相同
			return true;
		}
		if(person == null) {
			return false;
		}
		// 当对象传回到类之中的时候可以直接利用"对象.属性"访问
		if(this.name.equals(person.getName())&&this.age == person.getAge()) {
			return true;
		}else {
			return false;
		}
	}
	public String getName() {
		return this.name;
	}
	public int getAge() {
		return this.age;
	}
}

public class Ex3 {
	public static void main(String[] args) {
		Person perA = new Person("张三",20);
		Person perB = new Person("张三",20);
		if(perA.compare(perB)) {
			System.out.println("两个对象相等。");
		}else {
			System.out.println("两个对象不等。");
		}
	}
}

```



















































