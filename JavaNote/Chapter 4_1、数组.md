
# 一维数组：

定义数组并初始化时，长度无法进行初始化定义。

![](https://tcs.teambition.net/storage/3124d66e897ebfa0d2778c579845daeb6629?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkNjZlODk3ZWJmYTBkMjc3OGM1Nzk4NDVkYWViNjYyOSJ9.nlDBmqO_gGRSruwKGnEsDRxkJUa1qcJPicOXM_YGG9c&download=image.png "")

<br>

**范例：**
定义并使用数组

<br>

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[3]; // 表示开辟3个元素的数组
		System.out.println("数组长度：" + data.length);
		data[0] = 10;
		data[1] = 20;
		data[2] = 30;
		for(int x = 0;x<data.length;x++){
			System.out.println(data[x]);
		}
	}
}
```

<br>

**运行结果：**

![](https://tcs.teambition.net/storage/31257d8cc8b1808f769f9c192f6836f84c1a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU3ZDhjYzhiMTgwOGY3NjlmOWMxOTJmNjgzNmY4NGMxYSJ9.en6i07F9Mf3uBKh1eyPp3AG7204_HQ0n5SUjDLCTtqE&download=image.png "")

<br>

## 1、声明并开辟数组


```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[3]; // 表示开辟3个元素的数组
		System.out.println("数组长度：" + data.length);
		data[0] = 10;
		data[1] = 20;
		data[2] = 30;
		// 直接写“data”表示地址，而“data[下标]”表示访问元素
		int[] temp = data; //把data地址传递给temp，然后修改第一个元素
		temp[0] = 100;
		for(int x = 0;x<data.length;x++){
			System.out.println(data[x]);
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31255800c2dce5c1a1ce06a49a7bb2389666?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1ODAwYzJkY2U1YzFhMWNlMDZhNDlhN2JiMjM4OTY2NiJ9.SRaHC_gWynYh5jdZbDpLRWML3z2Ri0w5VPmopG4cMFk&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/3124ba1b65a52157c27dec9e127dc96f1392?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRiYTFiNjVhNTIxNTdjMjdkZWM5ZTEyN2RjOTZmMTM5MiJ9.xXvwhoFV1MMQha7YZ3M2RP1ixY9wR7cjDk8f89P6DFg&download=image.png "")

<br>

## 2、声明数组，为数组开辟空间（分步）

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = null; //声明数组
		data = new int[3]; // 开辟3个元素的数组
		System.out.println("数组长度：" + data.length);
		data[0] = 10;
		data[1] = 20;
		data[2] = 30;
		for(int x = 0;x<data.length;x++){
			System.out.println(data[x]);
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31259571ad833d2d08f4c9d017af66847b26?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU5NTcxYWQ4MzNkMmQwOGY0YzlkMDE3YWY2Njg0N2IyNiJ9.YYobNrihEduN-D8TlqKTmjXRgxh8x_okQ4IqwKLTWME&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/3124d8c0d112df67b802c754147deddce531?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkOGMwZDExMmRmNjdiODAyYzc1NDE0N2RlZGRjZTUzMSJ9.lS_9qO972LSchpWfUZK7PGYw7fJmNM1jx3EIGtqiELo&download=image.png "")

<br>

## 3、数组的静态初始化

![](https://tcs.teambition.net/storage/31248c9ae777a67b750f50331bd8e302957c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4YzlhZTc3N2E2N2I3NTBmNTAzMzFiZDhlMzAyOTU3YyJ9.paQRzMXlXQSzWQlIgDDVffSpVFD3NNCS8XQDkt0TxBE&download=image.png "")

<br>

**范例：**
数组的静态初始化


```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[]{4,3,6,5,7}; // 数组静态初始化
		for(int x = 0;x<data.length;x++){
			System.out.println(data[x]);
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31255df06e3f06f56d99dda3a762d689d849?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU1ZGYwNmUzZjA2ZjU2ZDk5ZGRhM2E3NjJkNjg5ZDg0OSJ9.Ct13Gr4SeUh86RS_avAFMyJnQiLjaBFuPpuIj9IbqWs&download=image.png "")

<br>

### 3.1、动态数组与静态数组：

- 动态数组：开辟的数组长度由用户决定，开辟之后的数据内容由系统来决定，系统认定的是对应数据类型的默认值。如 ：int data [] = new int [] ;

- 静态数组：开辟的数组长度由用户决定，开辟之后的数据内容由用户来初始化指定。并且数组的长度一定只能够使用“数组名称.length”取得。如： int data [] = new int [] {4,8,5,6,3} ;



## 4、数组排序：

<br>

**范例：**
一维数组排序，按从大到小排序


```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[]{4,3,6,5,7}; // 数组静态初始化
		for(int i = 0;i<data.length;i++){ //循环次数
			for(int j = 0;j<data.length-1;j++){
				if(data[j]<data[j+1]){ // 交换数据
					int temp = data[j];
					data[j] = data[j+1];
					data[j+1] = temp;
				}
			}
		}
		for(int x = 0;x<data.length;x++){
			System.out.print(data[x]+"、");
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125ae559f4dbad9375b63cec5004f110e97?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVhZTU1OWY0ZGJhZDkzNzViNjNjZWM1MDA0ZjExMGU5NyJ9.M9HqsjA1rJT_r4aHTR0DN70oWR6ENhThQ6G-T9AE6ks&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/31244faf90c3de57daa99abbb80fd0d18307?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0ZmFmOTBjM2RlNTdkYWE5OWFiYmI4MGZkMGQxODMwNyJ9.6nBkuNoJv8fyYAhhpWTrgVtFURM3aQqWPGKjdTmTX8o&download=image.png "")

<br>

### 4.1、不引入第3个变量实现数据交换：（数学原理）

![](https://tcs.teambition.net/storage/3124fd0b87a861c111639a1f47a44cb36117?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRmZDBiODdhODYxYzExMTYzOWExZjQ3YTQ0Y2IzNjExNyJ9.aohLVzFMHgBzBLF8YDegIsvifLIJunTVsYicE4z-5I8&download=image.png "")

<br>

**范例：**
一维数组排序，不引入第三个变量实现从小到大排序


```java
public class ArrayDemo {
	public static void main(String [] args){
		int [] data = new int []{4,3,2,5,6,8}; //数组静态初始化 
		double [] data1 = null; //数组动态初始化
		data1 = new double [3];
		data1[0] = 10;
		data1[1] = 20;
		data1[2] = 30;
		for(int i = 0;i<data.length;i++){ //循环次数
			for(int j = 0;j<data.length-1;j++){	//交换次数
				if(data[j]>data[j+1]){
//					int temp = data[j];	//引入第三个变量交换数据
//					data[j] = data[j+1];
//					data[j+1] = temp;
					data[j] = data[j]+data[j+1]; //不引入第三个变量交换数据
					data[j+1] = data[j]-data[j+1];
					data[j] = data[j]- data[j+1];
				}
			}
		}
		for(int x = 0;x<data.length;x++){
			System.out.print(data[x] + "、");
		}	
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/312597b529eb01b2c43a6d5aa6ba3bb94e7a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU5N2I1MjllYjAxYjJjNDNhNmQ1YWE2YmEzYmI5NGU3YSJ9.5DowBWx4PXfklM6rhipXFKSBQjh8akD1sNpuUjgmg6U&download=image.png "")

<br>

# 二维数组：（理解）

<br>

![](https://tcs.teambition.net/storage/31248f81da1a27a78340e2da2569037c73fa?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4ZjgxZGExYTI3YTc4MzQwZTJkYTI1NjkwMzdjNzNmYSJ9.o1W0UDyaZYbiNFqHlcJIOp4m0C0qzFWAYqtJp8rOcoA&download=image.png "")

<br>

![](https://tcs.teambition.net/storage/31244f3e7dfaf24c15e84522c6d52ad765d8?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0ZjNlN2RmYWYyNGMxNWU4NDUyMmM2ZDUyYWQ3NjVkOCJ9.8cy1VTdmXrFhJ1GK5mZFD8IM31dxCIaaQpD9BRYvR6E&download=image.png "")

<br>

**范例：**
定义二维数组

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[][] data = new int[][]{{1,2},{5,6,7,8},{9,10,20}}; // 二维数组静态初始化
		for(int x = 0;x<data.length;x++){  //控制行索引
			for(int y = 0;y<data[x].length;y++){  // 控制列索引
				System.out.print(data[x][y] + "、");
			}
			System.out.println();
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125eb0f4affcfe6d3796d2a45a4f9fa0696?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVlYjBmNGFmZmNmZTZkMzc5NmQyYTQ1YTRmOWZhMDY5NiJ9.6Clo8adMIETpNIcruVxEvMf49tUMuDHynhU-lfgk7kU&download=image.png "")

<br>

![](https://tcs.teambition.net/storage/31243556d29a04e2d4894724036c5884b076?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQzNTU2ZDI5YTA0ZTJkNDg5NDcyNDAzNmM1ODg0YjA3NiJ9.v813zKDqFilPS03veCFj8BGVJYowI5seBFrzFobTnDg&download=image.png "")

<br>

# 数组与方法的操作（难）

<br>

## 1、范例：让方法的参数接收数组


```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[]{1,3,5,7,9}; // 数组静态初始化
		printArray(data);
	}
	// 参数上明确表示要接收的数据是一个数组
	public static void printArray(int[] temp){
		for(int x = 0;x<temp.length;x++){
			System.out.print(temp[x] + "、");
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125c1021cfe6e8df6e60f2f1dec5dc07e26?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVjMTAyMWNmZTZlOGRmNmU2MGYyZjFkZWM1ZGMwN2UyNiJ9.-2T55-xtclZjPJH6rLInprxjrAnfKcmYyiKN_mDv1wg&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/31246870c087297c9c42462acbc5b35284dc?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ2ODcwYzA4NzI5N2M5YzQyNDYyYWNiYzViMzUyODRkYyJ9.gZnVEhz6K9VtZ4Q3_7eQconEdAS-rBjV1R_U_U0wJDc&download=image.png "")

<br>

## 2、范例：现在假设有一个int型数组，在里面有多个数据，如果要想判断某一个数据是否存在，该如何实现？

- 垃圾实现（别用）

![](https://tcs.teambition.net/storage/3124c89e8ed9fa10e14f65fdddb0929248d2?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjODllOGVkOWZhMTBlMTRmNjVmZGRkYjA5MjkyNDhkMiJ9.Imd6Com_K-aUgtg8cfVyVqvaWv8yEXzngwEoNmNgCqE&download=image.png "")

<br>

- 方法实现

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int searchData = 3; //待查找数据
		int[] data = new int[]{1,3,5,7,9};
		System.out.println(isExists(searchData,data) ? "查找到了!":"没有查找到!");
	}
	// 参数上明确表示要接收的数据是一个数组
	public static boolean isExists(int tempSearch,int[] arr){
		for(int x = 0;x<arr.length;x++){
			if(arr[x] == tempSearch){
				return true;  // 直接结束
			}
		}
		return false;
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/312583f2f06f16722b771d231c2655023756?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU4M2YyZjA2ZjE2NzIyYjc3MWQyMzFjMjY1NTAyMzc1NiJ9.IvgGGuVy_Zfj0tpx4worfuncsW6po-mOfrwOknw_Ano&download=image.png "")

<br>

开发原则：主方法之中的代码越少越好，主方法只需要调用方法就可以完成指定的功能。

- 利用方法减少客户端代码，在java之中有一个命名规范，如果说某一个方法返回的数据类型是boolean类型，一般此方法名称都要以 “isXxx()” 的形式命名。

<br>

## 3、范例：定义方法修改数组内容。

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[] {1,3,5,7,9};
		System.out.println("原始数组内容：");
		printArray(data);
		incrementDouble(data);
		System.out.println("修改后的数组内容：");
		printArray(data);
	}

	
	public static void incrementDouble(int arr[]) {
		for(int x = 0;x<arr.length;x++) {
			arr[x] *= 2;	//扩大两倍
		}
	}
	public static void printArray(int temp[]) {
		for(int x = 0;x<temp.length;x++) {
			boolean flag = false; 
			if(x < temp.length-1 ) {
				flag = true;
			}
			System.out.print(temp[x]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125f2ba2a942a73c4aa6a126e58de713da8?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVmMmJhMmE5NDJhNzNjNGFhNmExMjZlNThkZTcxM2RhOCJ9.D6wlrzoOJFSdBBGVeYNAXJq6N5rhhl2qAJ46bjIThr0&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/31248b0c51f93e66e81e6ddcaacc2ebd3c2a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4YjBjNTFmOTNlNjZlODFlNmRkY2FhY2MyZWJkM2MyYSJ9.9x_KqxC3dlVJjm1qEfGouClOlESSeWGP2TH746t3CMY&download=image.png "")

<br>

在引用数据类型操作之中，经常会出现在方法里面修改引用数据类型的形式，此时不要看代码，要回顾内存关系。

- 注意：引用数据类型之中最大的的特点是方法里面可以修改数组内容。

<br>

## 4、范例：定义方法返回数组


```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = init();
		printArray(data);
	}
	public static int[] init() {
		return new int[] {1,3,5,7,9};  //匿名数组
	}
	public static void printArray(int temp[]) {
		for(int x = 0;x<temp.length;x++) {
			boolean flag = false; 
			if(x < temp.length-1 ) {
				flag = true;
			}
			System.out.print(temp[x]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125980230f52c7273b2a367b8262b72e916?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU5ODAyMzBmNTJjNzI3M2IyYTM2N2I4MjYyYjcyZTkxNiJ9.FI3jAOA_uNUUG9zg5HrAsOlJI-L1AZ4eKrJYr4UbwDg&download=image.png "")

<br>

```java
//数组排序
//定义方法返回数组
//让方法的参数接收数组
public class ex4 {
	public static void arrayPrint(int [] array){
		for(int i = 0;i<array.length;i++) {
			boolean flag = false; 
			if(i < array.length-1 ) {
				flag = true;
			}
			System.out.print(array[i]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
	
	public static void main(String [] args) {
		int[] arry = new int[] {4,5,1,7,6,8,9,3};
		for(int i = 0;i<arry.length;i++) {  //控制循环次数
			for(int j = 0;j<arry.length-1;j++) {  //控制交换次数
				if(arry[j]>arry[j+1]) {
					int temp = arry[j];
					arry[j] = arry[j+1];
					arry[j+1] = temp; 
				}
			}
		}
		arrayPrint(arry); //打印输出
	} 
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125205b53a0fb99d93e08129f28a98261bd?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUyMDViNTNhMGZiOTlkOTNlMDgxMjlmMjhhOTgyNjFiZCJ9.fNbyHOsTdp9_Qd1SxNfBrF7xuT_IVmTAlDACXe4gyVY&download=image.png "")

<br>

## 5、范例：现在假设给出一个double型数组，要求定义一个方法，此方法可以统计出数组各个元素的和、平均值、最大值、最小值。

<br>

解题思路：一般一个方法只能够返回一个数据类型，但是现在需要返回的数据有四个，那么只能够将方法的返回值类型定义为数组，其中此数组第一个元素表示和，第二个元素表示平均值，第三个元素表示最大值，第四个元素表示最小值。

<br>

![](https://tcs.teambition.net/storage/31247347629a0f085b87eef8f8bc707be221?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3MzQ3NjI5YTBmMDg1Yjg3ZWVmOGY4YmM3MDdiZTIyMSJ9.lSrQqfhIvMaWJskvB_mV0XoAZPZsEcTPsupDLaswyXU&download=image.png "")

<br>

```java
public class Ex3 {
	public static void main(String[] args) {
		int[] data = new int [] {1,2,5,4,3,9};
		int[] result = init(data);
		System.out.println("和：" + result[0]);
		System.out.println("最大值：" + result[1]);
		System.out.println("最小值：" + result[2]);
		System.out.println("平均值：" + result[3]);
	}
	public static int[] init(int[] arry) {
		int sum = arry[0];  //保存元素之和
		int max = arry[0];  //第一个元素为最大值
		int min = arry[0];  //第一个元素为最小值
		for(int i = 0;i<arry.length;i++) {
			sum += arry[i];
			if(max < arry[i]) {
				max = arry[i];
			}
			if(min > arry[i]) {
				min = arry[i];
			}
		}
		int avg = sum /arry.length;  // 计算平均值
		return new int[] {sum,max,min,avg};
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/312519452e0802d315a5814eb13a942ac78b?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUxOTQ1MmUwODAyZDMxNWE1ODE0ZWIxM2E5NDJhYzc4YiJ9.EfKk6G6zlCuf3WiosDDaR7SmMVL1B0HnPxc60s1JKRw&download=image.png "")

<br>

### 面试题：请将一个数组进行转置

<br>

1. 情况一：转置的数组是一维数组。

- 原始数组：1、2、3、4、5、6、7、8、9

- 转置数组：9、8、7、6、5、4、3、2、1

    - 方法一：定义一个新数组，而后将原始数据倒着保存到新数组之后，再去改变原始数组的引用。（尽量避免使用）

        - 此方法一定会产生垃圾空间，而产生垃圾空间的代码我们应该尽量回避。

<br>

![](https://tcs.teambition.net/storage/3124cf06f5ce495cb0b2f1ad2c343f871e05?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjZjA2ZjVjZTQ5NWNiMGIyZjFhZDJjMzQzZjg3MWUwNSJ9.JVGrWVTJkrJelhBtrsbKgm4cQDui8Ux_tnuDQ8or8Mc&download=image.png "")

<br>

    - 方法二：实现数据的首尾交换。

        - 第一种情况：数组的长度为奇数长度。

        - 第二种情况：数组的长度为偶数长度。

奇数长度：

![](https://tcs.teambition.net/storage/31242e9c289203c5feed33136ec92f1065d0?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQyZTljMjg5MjAzYzVmZWVkMzMxMzZlYzkyZjEwNjVkMCJ9.QssHVKmk9B3MfYSXxN9N_WsqaXV5tgCtrXdCh90Arqc&download=image.png "")

偶数长度：

![](https://tcs.teambition.net/storage/3124a4011d9a9b18fbff87c02db36b5b53a9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRhNDAxMWQ5YTliMThmYmZmODdjMDJkYjM2YjViNTNhOSJ9.FxbTihKHTK7FAnQrUnYxVHLups9NDQzVzNy8GK1dhDY&download=image.png "")

<br>

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int [] {1,2,3,4,5,6,7,8,9};
		transpose(data);
		ArrayPrint(data);
	}
	public static void transpose(int arry[]) { //数组转置
		int centerPoit = arry.length / 2;  // 计算中间点，循环次数
		int head = 0;	// 左下标控制
		int bottom = arry.length-1;  // 右下标控制
		for(int i = 0;i<centerPoit;i++) {
			int temp = arry[head];
			arry[head] = arry[bottom];
			arry[bottom] = temp;
			head ++;
			bottom --;
		}
	}
	public static void ArrayPrint(int [] array){
		for(int i = 0;i<array.length;i++) {
			boolean flag = false; 
			if(i < array.length-1 ) {
				flag = true;
			}
			System.out.print(array[i]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/312501d2ebb63ec4dfd2f131bdb2d696d9e6?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUwMWQyZWJiNjNlYzRkZmQyZjEzMWJkYjJkNjk2ZDllNiJ9.o66AHVxq6FGQbsibZ7u-uYFPEaNezX6yESQyxv2WiJg&download=image.png "")

<br>

1. 情况二：转置的数组是二维数组。

转置前提：行和列相同

<br>

![](https://tcs.teambition.net/storage/3124a3d7e1a9bb2f55982c80f4bdc0abcbbd?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRhM2Q3ZTFhOWJiMmY1NTk4MmM4MGY0YmRjMGFiY2JiZCJ9.Bep2O2YztRXjCvRMETSQqliW6zed2OKzCyy4bnhk9XQ&download=image.png "")

<br>

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[][] data = new int[][] {
			{0,1,2},
			{3,4,5},
			{6,7,8}};
		reverse(data);
		printArray(data);
	}
	public static void reverse(int[][] arr) {
		for(int i = 0;i<arr.length;i++) {
			for(int j = 0;j<i;j++) {
				if(i != j) {  // 可以转换
					int temp = arr[i][j];
					arr[i][j] = arr[j][i];
					arr[j][i] = temp;
				}
			}
		}
	}
	public static void printArray(int temp[][]) {
		for(int x = 0;x<temp.length;x++) {
			for(int y = 0;y<temp[x].length;y++) {
				System.out.print(temp[x][y]);
				boolean flag = false; 
				if(y < temp[x].length-1 ) {
					flag = true;
				}
				System.out.print(flag ? "、" : ""); //三目表达式
			}
			System.out.println();
		}
		System.out.println();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125b5eabb864ed7972356942fc0ff72da16?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjViNWVhYmI4NjRlZDc5NzIzNTY5NDJmYzBmZjcyZGExNiJ9.Pb7X-2QpwAiUoG4VtNDws-2ZVq5BhPAqsEZ3QvbjEq8&download=image.png "")

<br>

# 与数组有关的操作方法

<br>

1、数组拷贝：

- 语法（不完整）：System.arraycopy(原数组名称，原数组开始点，目标数组名称，目标数组开始点，拷贝长度);

<br>

**范例：**
实现数组拷贝

- 数组一：1、2、3、4、5、6、7、8、9

- 数组二：11、22、33、44、55、66、77、88、99

- 拷贝后的数组一：1、2、3、55、66、77、7、8、9

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] dataA = new int[] {1,2,3,4,5,6,7,8,9};
		int[] dataB = new int[] {11,22,33,44,55,66,77,88,99};
		System.arraycopy(dataB,4,dataA,3,3);
		printArray(dataA);
	}
	public static void printArray(int temp[]) {
		for(int x = 0;x<temp.length;x++) {
			boolean flag = false; 
			if(x < temp.length-1 ) {
				flag = true;
			}
			System.out.print(temp[x]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31254450ef1a13e0faf96febb88cca88e1a0?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjU0NDUwZWYxYTEzZTBmYWY5NmZlYmI4OGNjYTg4ZTFhMCJ9.Hj_a9xeHmmTtMIbTi7xbrBlDr0dqsCWpBZsY0naxOPY&download=image.png "")

<br>

**思考题：**
在原有数组{1，3，5，7}上，扩充数组容量为2

- 扩充容量，数组的长度永恒都是固定的，所以此时只能够开辟一个新的数组，新数组有新的长度；

- 原始数据保留，应该在新数组之中保存已有的数据，则表示将旧的数据拷贝到新数组之中。

<br>

这样并不标准：

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[] {1,3,5,7};
		data = increment(data, 2);  //改变引用关系
		printArray(data);
	}
	public static int[] increment(int[] temp,int len) {
		int[] newArr = new int[temp.length + len];
		System.arraycopy(temp, 0, newArr, 0, temp.length);
		return newArr;  // 返回新数组
	}
	public static void printArray(int temp[]) {
		for(int x = 0;x<temp.length;x++) {
			boolean flag = false; 
			if(x < temp.length-1 ) {
				flag = true;
			}
			System.out.print(temp[x]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/31253cb2e35e11a82451effb13368ae3577b?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjczMzEwNSwiaWF0IjoxNjIyMTI4MzA1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUzY2IyZTM1ZTExYTgyNDUxZWZmYjEzMzY4YWUzNTc3YiJ9.iKt5SC1ecp5M4IHrWkssQfZMNxWCNlhx3QOYyStINWE&download=image.png "")

<br>

2、数组排序：

- 语法：java.util.Arrays.sort(数组名称);

![](https://tcs.teambition.net/storage/31247ff05b5d699dc37302c6d26cdde6ded9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3ZmYwNWI1ZDY5OWRjMzczMDJjNmQyNmNkZGU2ZGVkOSJ9.x3SqYRPhOeoMVWXXycFPuT7c1iXp1pTGOkz2TXzZzQ4&download=image.png "")

```java
public class ArrayDemo {
	public static void main(String[] args) {
		int[] data = new int[] {8,6,1,0,10,20,3};
		java.util.Arrays.sort(data);
		printArray(data);
	}
	public static void printArray(int temp[]) {
		for(int x = 0;x<temp.length;x++) {
			boolean flag = false; 
			if(x < temp.length-1 ) {
				flag = true;
			}
			System.out.print(temp[x]);
			System.out.print(flag ? "、" : ""); //三目表达式
		}
		System.out.println();
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/3125aef9329fba179683025774e298223f93?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjczMzQ3OSwiaWF0IjoxNjIyMTI4Njc5LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVhZWY5MzI5ZmJhMTc5NjgzMDI1Nzc0ZTI5ODIyM2Y5MyJ9.LzgvPJHQCPEBnThCqFOLvD_I0LQQWiVZpIjaR4TqhZM&download=image.png "")

<br>

# 对象数组（重点）

<br>

对象数组包含的一定是多个操作对象。

![](https://tcs.teambition.net/storage/3124c42c3bcbf662eb5bf6a47d667e70ecc1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjNDJjM2JjYmY2NjJlYjViZjZhNDdkNjY3ZTcwZWNjMSJ9.0zeWHM29l2QiFLiOpIhs18ALJ8IKTyTBaIwOxPG_1xY&download=image.png "")

<br>

范例：动态数组初始化

```java
class Person{
	private String name;
	private int age;
	public Person(String n,int a) {
		name = n;
		age = a;
	}  // setter、getter略
	public String getInfo() {
		return "姓名：" + name + "，年龄：" + age;
	}
}

public class ArrayDemo {
	public static void main(String[] args) {
		Person[] per = new Person[3];   // 对象数组
		per[0] = new Person("张三", 20);
		per[1] = new Person("李四", 21);
		per[2] = new Person("王五", 22);
		for(int x = 0;x<per.length;x++) {
			System.out.println(per[x].getInfo());
		}
	}
}
```

**运行结果：**

![](https://tcs.teambition.net/storage/3125a660558397a0befed354c491df829c99?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjczMzkzMCwiaWF0IjoxNjIyMTI5MTMwLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjVhNjYwNTU4Mzk3YTBiZWZlZDM1NGM0OTFkZjgyOWM5OSJ9.AhUS-cHcZUlCBdINhDwbpN99Nb6QY3GiXGgZdey8_HQ&download=image.png "")

<br>

**内存图：**

![](https://tcs.teambition.net/storage/31245ee144aa239952a7eca725decf8f01dc?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ1ZWUxNDRhYTIzOTk1MmE3ZWNhNzI1ZGVjZjhmMDFkYyJ9.OopI3R9wVuu4-X6iHgcfJLYKx33OkgKmRvq5TKs2IfI&download=image.png "")

<br>

范例：静态数组初始化

写法一：

```java
class Person{
	private String name;
	private int age;
	public Person(String n,int a) {
		name = n;
		age = a;
	}  // setter、getter略
	public String getInfo() {
		return "姓名：" + name + "，年龄：" + age;
	}
}

public class ArrayDemo {
	public static void main(String[] args) {
		Person[] per = new Person[] {
			new Person("张三", 20),
			new Person("李四", 21),
			new Person("王五", 22)};   // 对象数组
		for(int x = 0;x<per.length;x++) {
			System.out.println(per[x].getInfo());
		}
	}
}

```

**运行结果：**

![](https://tcs.teambition.net/storage/312539729809b6e5968743c4772726fe8f56?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjczNDE0OCwiaWF0IjoxNjIyMTI5MzQ4LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUzOTcyOTgwOWI2ZTU5Njg3NDNjNDc3MjcyNmZlOGY1NiJ9.DA5t2-bZfFPWvxgVf_A5J1cvZKSiYNiWzLNwfZQlKyg&download=image.png "")

<br>

写法二：

```java
class Person{
	private String name;
	private int age;
	public Person(String n,int a) {
		name = n;
		age = a;
	}  // setter、getter略
	public String getInfo() {
		return "姓名：" + name + "，年龄：" + age;
	}
}

public class ArrayDemo {
	public static void main(String[] args) {
			Person perA = new Person("张三", 20);
			Person perB = new Person("李四", 21);
			Person perC = new Person("王五", 22);
			Person[] per = new Person[] {perA,perB,perC};   // 对象数组
		for(int x = 0;x<per.length;x++) {
			System.out.println(per[x].getInfo());
		}
	}
}
```
<br>

**运行结果：**

![](https://tcs.teambition.net/storage/312533bc7d1116e6ff51b49dbda45385d0e1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IjVmYzRhYjcxYTNkYmY4NTljODhlMzdiNSIsImV4cCI6MTYyMjczNDIxMSwiaWF0IjoxNjIyMTI5NDExLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjUzM2JjN2QxMTE2ZTZmZjUxYjQ5ZGJkYTQ1Mzg1ZDBlMSJ9.qbpcmTHcCzNHzumcFy54mqf70a6WbDQXyTbnitFmPUs&download=image.png "")

<br>

# 总结：

![](https://tcs.teambition.net/storage/31247c2a884269adac6e27db00bde6ed953e?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3YzJhODg0MjY5YWRhYzZlMjdkYjAwYmRlNmVkOTUzZSJ9.LMQdn9npUjkFbIw9BhAGJaWIbjsCOKdIoMFPJ0CyKDg&download=image.png "")

![](https://tcs.teambition.net/storage/31247e951f30b28e5a615b2a3fd93213b8f1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjczMjUxNSwiaWF0IjoxNjIyMTI3NzE1LCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3ZTk1MWYzMGIyOGU1YTYxNWIyYTNmZDkzMjEzYjhmMSJ9.ueuKzVWX2AZJoV5k5MPCuVyX9gfSiOep8U6_ifo3ew0&download=image.png "")

