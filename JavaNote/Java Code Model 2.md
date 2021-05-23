# 2、第二个代码模型：数据表与简单java类映射（核心）



**题目：**使用emp雇员表（empno、ename、job、sal、comm、*mgr*、*deptno*）和dept部门表（*deptno*、dname、loc）实现以下功能：其中mgr、deptno为关联字段

- 功能一：可以输出部门的完整信息，同时输出部门之中所有雇员直接领导的信息；

- 功能二：可以根据一个雇员找到雇员的领导信息和他所在的部门信息。

在本题目之中有两个关联的对应关系：

- 关系一：雇员和部门之间依靠的deptno字段的联系；

- 关系二：雇员和领导之间的联系，依靠mgr字段。



**步骤一：**编写简单java类，暂时只包含表之中的基本字段。

```java
class Emp{
	private int empno;
	private String ename;
	private String job;
	private double sal ;
	private double comm;
	public Emp(){}
	public Emp(int empno,String ename,String job,double sal,double comm){
		this.empno = empno;
		this.ename = ename;
		this.job = job;
		this.sal = sal;
		this.comm = comm;
	}
	public String getInfo(){
		return "雇员编号：" + this.empno +
			   "，雇员姓名：" + this.ename +				
			   "，职位：" + this.job +
			   "，工资：" + this.sal +
			   "，佣金：" + this.comm ;
	}
}

class Dept{
	private int deptno;
	private String dname;
	private String loc;
	public Dept(){}
	public Dept(int deptno,String dname,String loc){
	this.deptno = deptno;
	this.dname = dname;
	this.loc = loc;
	}	
	public String getInfo(){
		return "部门编号：" + this.deptno +
			   "，部门名称" + this.dname +
			   "，部门位置" + this.loc ;
	}
}

public class TestDemo{
	public static void main(String[] args){
		//第一层次：设置关系
		//第二层次：根据关系取数据
	}
}
```



**步骤二：**设置关系字段

- 一对多关系：部门和雇员；

- 一对多关系：雇员和领导。

```java
//雇员类
class Emp{
	private int empno;
	private String ename;
	private String job;
	private double sal ;
	private double comm;
	private Dept dept; //一个雇员属于一个部门
	private Emp mgr;
	public Emp(){}
	public Emp(int empno,String ename,String job,double sal,double comm){
		this.empno = empno;
		this.ename = ename;
		this.job = job;
		this.sal = sal;
		this.comm = comm;
	}
	public void setDept(Dept dept){
		this.dept = dept;
	}
	public Dept getDept(){
		return this.dept;
	}
	public void setMgr(Emp mgr){
		this.mgr = mgr;
	}
	public Emp getMgr(){
		return this.mgr;
	}
	public String getInfo(){
		return "雇员编号：" + this.empno +
			   "，雇员姓名：" + this.ename +				
			   "，职位：" + this.job +
			   "，工资：" + this.sal +
			   "，佣金：" + this.comm ;
	}
}

//部门类
class Dept{
	private int deptno;
	private String dname;
	private String loc;
	private Emp[] emps ; //多个雇员
	public Dept(){}
	public Dept(int deptno,String dname,String loc){
	this.deptno = deptno;
	this.dname = dname;
	this.loc = loc;
	}
	public void setEmps(Emp[] emps){
		this.emps = emps;
	}
	public Emp[] getEmps(){
		return this.emps;
	}
	public String getInfo(){
		return "部门编号：" + this.deptno +
			   "，部门名称" + this.dname +
			   "，部门位置" + this.loc ;
	}
}

public class TestDemo{
	public static void main(String[] args){
		//第一层次：设置关系
		//第二层次：根据关系取数据
	}
}
```



**步骤三：**按照表结构设置数据，同时设置完数据后按照表结构取出数据

```java
//雇员类
class Emp{
	private int empno;
	private String ename;
	private String job;
	private double sal ;
	private double comm;
	private Dept dept; //一个雇员属于一个部门
	private Emp mgr;
	public Emp(){}
	public Emp(int empno,String ename,String job,double sal,double comm){
		this.empno = empno;
		this.ename = ename;
		this.job = job;
		this.sal = sal;
		this.comm = comm;
	}
	public void setDept(Dept dept){
		this.dept = dept;
	}
	public Dept getDept(){
		return this.dept;
	}
	public void setMgr(Emp mgr){
		this.mgr = mgr;
	}
	public Emp getMgr(){
		return this.mgr;
	}
	public String getInfo(){
		return "雇员编号：" + this.empno +
			   "，雇员姓名：" + this.ename +				
			   "，职位：" + this.job +
			   "，工资：" + this.sal +
			   "，佣金：" + this.comm ;
	}
}

//部门类
class Dept{
	private int deptno;
	private String dname;
	private String loc;
	private Emp[] emps ; //多个雇员
	public Dept(){}
	public Dept(int deptno,String dname,String loc){
	this.deptno = deptno;
	this.dname = dname;
	this.loc = loc;
	}
	public void setEmps(Emp[] emps){
		this.emps = emps;
	}
	public Emp[] getEmps(){
		return this.emps;
	}
	public String getInfo(){
		return "部门编号：" + this.deptno +
			   "，部门名称" + this.dname +
			   "，部门位置" + this.loc ;
	}
}

public class TestDemo{
	public static void main(String[] args){
		// 第一层次：设置关系
		// 1、分别设置各个对象实体，彼此之间没有联系
		Emp ea = new Emp(1001,"person1","java",1000.0,0.0);
		Emp eb = new Emp(1002,"person2","c",2000.0,0.0);
		Emp ec = new Emp(1003,"person3","c++",3000.0,0.0);
		Dept dept = new Dept(2000,"ACCOUNTING","China");
		// 2、设置雇员和领导关系
		ea.setMgr(eb);
		eb.setMgr(ec); // ec没有领导
		// 3、设置雇员和部门关系
		ea.setDept(dept); // 雇员和部门
		eb.setDept(dept); // 雇员和部门
		ec.setDept(dept); // 雇员和部门
		dept.setEmps(new Emp[] {ea,eb,ec});
		// 第二层次：根据关系取数据
		// 1、取出部门信息
		System.out.println(dept.getInfo());
		// 2、取出部门之中的所有雇员信息
		for(int i = 0;i<dept.getEmps().length;i++){
			Emp e = dept.getEmps()[i]; //取出一个雇员
			System.out.println("\t" + e.getInfo());
			if(e.getMgr() != null){// 有领导
				System.out.println("\t\t|- " + e.getMgr().getInfo());
			}
		}
		// 3、根据雇员取信息
		System.out.println(ea.getInfo());
		if(ea.getMgr() != null){
			System.out.println(ea.getMgr().getInfo());
		}
		if(ea.getDept() != null){
			System.out.println(ea.getDept().getInfo());
		}
	}
}
```



运行结果**：**

![](https://tcs.teambition.net/storage/31256423484c9a89f7fe02a92bc5cc40680c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjM2Mzg1OSwiaWF0IjoxNjIxNzU5MDU5LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU2NDIzNDg0YzlhODlmN2ZlMDJhOTJiYzVjYzQwNjgwYyJ9.aly4t65ij9N9NS7XZ42ST0etK6VflDPpEg5Ec2Hm9BA&download=image.png "")































































