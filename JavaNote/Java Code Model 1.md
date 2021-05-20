# 1、第一个代码模型：简单Java类编写（核心）



所谓的简单Java类指的是类的组成结构单一，只包含了最基本的属性与属性的设置和取得功能（即setter和getter方法）。并且在我们日后的所有的开发之中都是基于简单Java类的应用，那么本次首先给出简单Java类开发的基本的原则：

-  类名称必须有意义，并且可以明确的表示出某一类事物，例如：学生、老师；

- 类之中的所有属性必须使用private封装，而且所有的属性必须编写相应的setter、getter方法；

- 类之中可以定义多个构造方法，但是不管有多少个请一定要保证有一个无参构造方法；

- 类中不允许直接输出，即不可以编写任何的 “System.out.println()” 语句，所有的输出要返回给被调用处； 

- 类中需要编写一个可以取得对象完整信息的方法，此处暂时定义为getInfo()，返回值为String。





## 例子：定义一个表示学生的类，类之中包含有学生的编号、姓名、年龄。

```java
class Student{
	private int sId;
	private String sName;
	private int sAge;
	public Student() {}		//无参构造方法
	public Student(int id , String name , int age) {
		this.setSId(id);
		this.setSName(name);
		this.setSAge(age);
	}
	public void setSId(int id){
		this.sId = id;
	}
	public void setSName(String name) {
		this.sName = name;
	}
	public void setSAge(int age){
		this.sAge = age;
	}
	public int getSId() {
		return sId;
	}
	public String getSName() {
		return sName;
	}
	public int getSAge() {
		return sAge;
	}
	public String getInfo() {
		return " 学生信息：" + "\n"+
				"sId = "   + this.getSId() + "\n" +
				"sName = " + this.getSName() + "\n" +
				"sAge = "  + this.getSAge();
	}
}

public class ex1 {
	public static void main(String[] args) {
		System.out.println(new Student(1808010240, "公主小鸟", 23).getInfo());
	}
}

```





















