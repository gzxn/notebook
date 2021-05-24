
# **回顾：**

**1、String 类的主要特点：**

- String类对象有两种实例化方式：

    - 直接赋值（String str = "字符串"）：开辟一块内存空间，可以自动保存在对象池之中供下次使用；

    - 使用关键字new调用构造方法（String str = new String("字符串")）：开辟两块内存空间，其中有一块空间将成为垃圾，不会自动入池，但可以使用intern()方法手工入池；

- String类对象有两种比较方式：

    - “==”：比较的是两个对象的地址数值，属于数值比较；

    - ”equals()”：比较涩是两个字符串对象的内容，在equals()之中可以进行null的判断；

- 一个字符串常量就属于String类的匿名对象，所以字符串一旦定义则不可改变，而字符串对象内容的修改依靠的是字符串对象的引用

**2、this关键字：**

- 使用“this.属性”表示本类属性。

- 使用“this.方法()”可以调用本类普通方法，而使用“this()”表示调用本类构造方法，而且此代码要求放在构造方法的首行，并且要多个构造之间不允许循环调用，还要留一个出口。

- this表示当前对象：当前正在调用本类中方法的对象。

<br>
<br>

![](https://tcs.teambition.net/storage/31257fb6982e64069d187a64c56d319e2e3a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjQ0NzcyNywiaWF0IjoxNjIxODQyOTI3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU3ZmI2OTgyZTY0MDY5ZDE4N2E2NGM1NmQzMTllMmUzYSJ9.EOjvBhWmIc4Z0rqRNE_kiVx3xbCETyg3zHIkYSGSTis&download=image.png "")


```java
class Type{
	private int tid; // 类别编号
	private String name; // 类别名称
	private String note; // 描述
	private SubType[] subTypes; // 子类别
	public Type() {}
	public Type(int tid,String name,String note) {
		this.tid = tid;
		this.name = name;
		this.note = note;
	}
	public void setSubTypes(SubType[] subTypes) {
		this.subTypes = subTypes;
	}
	public SubType[] getSubTypes() {
		return this.subTypes;
	}
	public String getInfo() {
		return "类别编号：" + this.tid + "，名称：" + this.name + "，描述：" + this.note;
	}
}

class SubType{
	private int stid; // 子类别编号
	private String name; // 子类别名称
	private String note; // 描述
	private Type type; // 类别
	public SubType() {}
	public SubType(int stid,String name,String note) {
		this.stid = stid;
		this.name = name;
		this.note = note;
	}
	public void setType(Type type) {
		this.type = type;
	}
	public Type getType() {
		return this.type;
	}
	public String getInfo() {
		return "子类别编号：" + this.stid + "，名称：" + this.name + "，描述：" +this.note;
	}
}

public class Ex1 {
	public static void main(String[] args) {
		//第一层次：设置关系
		Type type = new Type(1,"图像视频处理","处理照片、影片");
		SubType st1 = new SubType(100,"图片编辑","--");
		SubType st2 = new SubType(200,"动画设计","--");
		SubType st3 = new SubType(300,"视频处理","--");
		st1.setType(type);
		st2.setType(type);
		st3.setType(type);
		type.setSubTypes(new SubType[] {st1,st2,st3});
		//第二层次：根据关系取数据
		System.out.println(type.getInfo());
		for(int i = 0;i<type.getSubTypes().length;i++) {
			System.out.println("\t|-" + type.getSubTypes()[i].getInfo());
		}
	}
}

```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/3125248f8dc791e03d52e757cd46c8c9e4c4?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjQ1MTk3NCwiaWF0IjoxNjIxODQ3MTc0LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUyNDhmOGRjNzkxZTAzZDUyZTc1N2NkNDZjOGM5ZTRjNCJ9.Ol8r4l7j3WrKOIu0HoKRDFGt5IqD3O2dkIimfkxVB0w)

<br>

![](https://tcs.teambition.net/storage/3125df66882fe4f9fe07a72f46ec3fc8d98a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjQ0NzcyNywiaWF0IjoxNjIxODQyOTI3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVkZjY2ODgyZmU0ZjlmZTA3YTcyZjQ2ZWMzZmM4ZDk4YSJ9.SF0kY6XC2k2J1P7hLOUUzOeJFTwYO5LiKEL4-gNhfvI&download=image.png "")


```java
class User{
	private String uid;
	private String password;
	private int flag;
	private int level;
	private int grade;
	private Log[] logs;
	public User() {}
	public User(String uid,String password,int flag,int level,int grade) {
		this.uid = uid;
		this.password = password;
		this.flag = flag;
		this.level = level;
		this.grade = grade;
	}
	public void setLogs(Log[] logs) {
		this.logs = logs;
	}
	public Log[] getLogs() {
		return this.logs;
	}
	public String getInfo() {
		return "用户编号：" + this.uid + 
				"，密码：" + this.password + 
				"，审核标志位：" +(this.flag == 0 ? "已审核" : "未审核")+ 
				"，级别：" + this.level + 
				"，积分：" + this.grade;
	}
}

class Log{
	private int lid;
	private String ip;
	private User user;
	public Log() {}
	public Log(int lid,String ip) {
		this.lid = lid;
		this.ip = ip;
	}
	public void setUser(User user) {
		this.user = user;
	}
	public User getUser() {
		return this.user;
	}
	public String getInfo() {
		return "用户登录日志编号：" + this.lid + "，IP地址：" + this.ip;
	}
}

public class Ex2 {
	public static void main(String[] args) {
		//第一层次：设置关系
		User user = new User("admin","123456",0,1,10);
		Log logA = new Log(1,"10.10.10.10");
		Log logB = new Log(2,"100.100.100.100");
		Log logC = new Log(3,"200.200.200.200");
		logA.setUser(user);
		logB.setUser(user);
		logC.setUser(user);
		user.setLogs(new Log[] {logA,logB,logC});
		//第二层次：根据关系取数据
		System.out.println(user.getInfo());
		for(int i = 0;i<user.getLogs().length;i++) {
			System.out.println("\t|-" + user.getLogs()[i].getInfo());
		}
	}
}

```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31254e1d998bbadc780b48b01634900bd972?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjQ0OTkyNiwiaWF0IjoxNjIxODQ1MTI2LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU0ZTFkOTk4YmJhZGM3ODBiNDhiMDE2MzQ5MDBiZDk3MiJ9.zNo_1-BWSIjeBU3_xzpPUui9zqcqp6S2wRLLFgl0ErY&download=image.png "")

<br>

![](https://tcs.teambition.net/storage/3125ef5f09dab207d7ef3ebd9bde433be255?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjQ0NzcyNywiaWF0IjoxNjIxODQyOTI3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVlZjVmMDlkYWIyMDdkN2VmM2ViZDliZGU0MzNiZTI1NSJ9.RRUqqBQOQ2OgyT6bHol2RRjJ0OveiJtEM8z1sKlJHW0&download=image.png "")


```java
class Admin{
	private String aid;
	private String password;
	private int flag;
	private Group[] groups;
	public Admin() {}
	public Admin(String aid,String password,int flag) {
		this.aid = aid;
		this.password = password;
		this.flag = flag;
	}
	public void setGroups(Group[] groups) {
		this.groups = groups;
	} 
	public Group[] getGroups() {
		return this.groups;
	}
	public String getInfo() {
		return "管理员编号：" + this.aid + "，密码：" + this.password + "，超级管理员标志：" + (this.flag == 0 ? "超级管理员":"普通管理员");
	}
}

class Group{
	private int gid;
	private String name;
	private String note;
	private Admin[] admins;
	private Privilege[] privileges;
	public Group(){}
	public Group(int gid,String name,String note) {
		this.gid = gid;
		this.name = name;
		this.note = note;
	}
	public void setAdmins(Admin[] admins) {
		this.admins = admins;
	}
	public Admin[] getAdmins() {
		return this.admins;
	}
	public void setPrivileges(Privilege[] privileges) {
		this.privileges = privileges;
	}
	public Privilege[] getPrivileges() {
		return this.privileges;
	}
	public String getInfo() {
		return "管理员组编号：" + this.gid + "，名称：" + this.name + "，描述：" + this.note;
	}
}

class Privilege{
	private int pid;
	private String name;
	private String url;
	private Group[] groups;
	public Privilege() {}
	public Privilege(int pid,String name,String url) {
		this.pid = pid;
		this.name = name;
		this.url = url;
	}
	public void setGroups(Group[] groups) {
		this.groups = groups;
	}
	public Group[] getGroups() {
		return this.groups;
	}
	public String getInfo() {
		return "权限编号：" + this.pid + "，名称：" + this.name + "，URL：";
	}
}

public class Ex3 {
	public static void main(String[] argds) {
		// 第一层次：设置关系
		// 1、设置管理员数据
		Admin a1 = new Admin("超级管理员","hello",0);
		Admin a2 = new Admin("数据管理员","hello",1);
		Admin a3 = new Admin("信息管理员","hello",1);
		//2、设置管理员组
		Group g1 = new Group(1,"超级管理员组","--");
		Group g2 = new Group(2,"普通管理员组","--");
		// 3、设置权限数据
		Privilege priA = new Privilege(1001,"管理员维护","--");
		Privilege priB = new Privilege(1002,"业务维护","--");
		Privilege priC = new Privilege(1003,"数据员维护","--");
		Privilege priD = new Privilege(1004,"审核维护","--");
		Privilege priE = new Privilege(1005,"员工维护","--");
		//4、设置管理员和管理员组的关系
		a1.setGroups(new Group[] {g1,g2});
		a2.setGroups(new Group[] {g2});
		a3.setGroups(new Group[] {g2});
		g1.setAdmins(new Admin[] {a1});
		g2.setAdmins(new Admin[] {a1,a2,a3});
		//5、设置管理员组和权限关系
		g1.setPrivileges(new Privilege[] {priA,priB,priC,priD,priE});
		g2.setPrivileges(new Privilege[] {priB,priC,priD});
		priA.setGroups(new Group[] {g1});
		priB.setGroups(new Group[] {g1,g2});
		priC.setGroups(new Group[] {g1,g2});
		priD.setGroups(new Group[] {g1,g2});
		priE.setGroups(new Group[] {g1});
		// 第二层次：根据关系取数据
		// 1、根据一个管理员取得次管理员所在的所有管理员组，以及每一个管理员组所具备的权限。
		System.out.println(a1.getInfo());
		for(int i = 0;i<a1.getGroups().length;i++) {
			System.out.println("\t|-" + a1.getGroups()[i].getInfo());
			for(int j = 0;j<a1.getGroups()[i].getPrivileges().length;j++) {
				System.out.println("\t\t|-" + a1.getGroups()[i].getPrivileges()[j].getInfo());
			}
		}
		System.out.println("=========================================");
		// 2、 根据一个管理员组取得此管理员组下所有管理员和权限信息。
		System.out.println(g1.getInfo());
		for(int i = 0;i<g1.getAdmins().length;i++) {
			System.out.println("\t|-" + g1.getAdmins()[i].getInfo());
		}
		for(int i = 0;i<g1.getPrivileges().length;i++) {
			System.out.println("\t|-" + g1.getPrivileges()[i].getInfo());
		}
		System.out.println("=========================================");
		// 3、根据一个权限取得具备此权限的所有管理员组，以及每个管理员组的管理员信息。
		System.out.println(priC.getInfo());
		for(int i = 0;i<priC.getGroups().length;i++) {
			System.out.println("\t|-" + priC.getGroups()[i].getInfo());
			for(int j = 0;j<priC.getGroups()[i].getAdmins().length;j++) {
				System.out.println("\t\t|-" + priC.getGroups()[i].getAdmins()[j].getInfo());	
			}
		}
	}
}

```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/3125dac4b3eee5c87a558458d2be54c8a1f2?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjQ0NzcyNywiaWF0IjoxNjIxODQyOTI3LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVkYWM0YjNlZWU1Yzg3YTU1ODQ1OGQyYmU1NGM4YTFmMiJ9.TOePmwLq_6jav6LFSf8_Cw3d96FZy7HzT3WG5mrMeSY&download=image.png "")

























































































