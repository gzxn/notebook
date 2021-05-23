

# 一维数组：

定义数组并初始化时，长度无法进行初始化定义。

![](https://tcs.teambition.net/storage/3124d66e897ebfa0d2778c579845daeb6629?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkNjZlODk3ZWJmYTBkMjc3OGM1Nzk4NDVkYWViNjYyOSJ9.NLOArbyQ5fZ6X2eL3U0Uklj9h_m1pWv2TtmTbC9IGys&download=image.png "")



![](https://tcs.teambition.net/storage/31241b687ef400d909d3de1e394b5d2b2b08?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQxYjY4N2VmNDAwZDkwOWQzZGUxZTM5NGI1ZDJiMmIwOCJ9.YVTv4ZmzGtmxKekx2x9gA8dXcpmNnAZbOSj1COYMqXs&download=image.png "")



## 1、声明并开辟数组

![](https://tcs.teambition.net/storage/3124b41e66184dca9010ab1c81e04944a160?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRiNDFlNjYxODRkY2E5MDEwYWIxYzgxZTA0OTQ0YTE2MCJ9.sitLuNN3lECAw0lKO_5x2Wl8nsiqB6KHKyT7dxVerkQ&download=image.png "")

![](https://tcs.teambition.net/storage/3124ba1b65a52157c27dec9e127dc96f1392?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRiYTFiNjVhNTIxNTdjMjdkZWM5ZTEyN2RjOTZmMTM5MiJ9.Vg_jWXp5Ul09XhocQsHDeT_m-txoHrU4KCkR8F_7DDU&download=image.png "")



## 2、声明数组，为数组开辟空间

![](https://tcs.teambition.net/storage/31245005f644955ca3a9ca21368d95456e60?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ1MDA1ZjY0NDk1NWNhM2E5Y2EyMTM2OGQ5NTQ1NmU2MCJ9.uwlFFTskq_l6wx4VFXgJJP8TQuhTLDDBmyj3cpiTLXo&download=image.png "")

![](https://tcs.teambition.net/storage/3124d8c0d112df67b802c754147deddce531?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkOGMwZDExMmRmNjdiODAyYzc1NDE0N2RlZGRjZTUzMSJ9.Uz_hZKlAKz3fFNUrvzQItocDx4Yl3dC5-S9A8E6-y3s&download=image.png "")



## 3、数组的静态初始化

![](https://tcs.teambition.net/storage/31248c9ae777a67b750f50331bd8e302957c?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4YzlhZTc3N2E2N2I3NTBmNTAzMzFiZDhlMzAyOTU3YyJ9.qF4QfmLDiFaJfEPIkTcR20oribxO_2_NVrPM8oMmZZA&download=image.png "")



![](https://tcs.teambition.net/storage/31244e3046405080134d179c36ffe6588654?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0ZTMwNDY0MDUwODAxMzRkMTc5YzM2ZmZlNjU4ODY1NCJ9.YaNrMY0wOs-Nvea4dZW5biaNE1fg55Wfo0t-Q0aYk4Q&download=image.png "")

### 3.1、动态数组与静态数组：

- 动态数组：开辟的数组长度由用户决定，开辟之后的数据内容由系统来决定，系统认定的是对应数据类型的默认值。如 ：int data [] = new int [] ;

- 静态数组：开辟的数组长度由用户决定，开辟之后的数据内容由用户来初始化指定。并且数组的长度一定只能够使用“数组名称.length”取得。如： int data [] = new int [] {4,8,5,6,3} ;


## 4、数组排序：

![](https://tcs.teambition.net/storage/3124519122875f4585dea1cea5ed1609cda4?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ1MTkxMjI4NzVmNDU4NWRlYTFjZWE1ZWQxNjA5Y2RhNCJ9.ODuE30QD9Q83Uq2zurv-RGwuobM_txCd6L7rgG8J08s&download=image.png "")

![](https://tcs.teambition.net/storage/31244faf90c3de57daa99abbb80fd0d18307?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0ZmFmOTBjM2RlNTdkYWE5OWFiYmI4MGZkMGQxODMwNyJ9.GCwz1NiTAQaAgSZEV0qBfs5k-nQfZNPbKuUgT6_Z-DQ&download=image.png "")

### 4.1、不引入第3个变量实现数据交换：

![](https://tcs.teambition.net/storage/3124fd0b87a861c111639a1f47a44cb36117?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRmZDBiODdhODYxYzExMTYzOWExZjQ3YTQ0Y2IzNjExNyJ9.F83I4uvH6eUc40uqTZHhVuD2y4yehc9fXWJ7xVRAobY&download=image.png "")

```java
public class Ex1 {
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

# 二维数组：（理解）

![](https://tcs.teambition.net/storage/31248f81da1a27a78340e2da2569037c73fa?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4ZjgxZGExYTI3YTc4MzQwZTJkYTI1NjkwMzdjNzNmYSJ9.ZpZryk9A3L0dY8uIO1WrGLHbtz-aSgwtcMORUn0bxLg&download=image.png "")

![](https://tcs.teambition.net/storage/31244f3e7dfaf24c15e84522c6d52ad765d8?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0ZjNlN2RmYWYyNGMxNWU4NDUyMmM2ZDUyYWQ3NjVkOCJ9.etNkQhL7tI38denRjlEUWM41_OgrS5BgV-GDCQfemSA&download=image.png "")

![](https://tcs.teambition.net/storage/3124fdaf328e6f5d3baea389fb699a28a6ef?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRmZGFmMzI4ZTZmNWQzYmFlYTM4OWZiNjk5YTI4YTZlZiJ9.IBkp6MKMyo31gdnjckTfrtLhcSydF7IF0VnnnmhuQwY&download=image.png "")

![](https://tcs.teambition.net/storage/31243556d29a04e2d4894724036c5884b076?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQzNTU2ZDI5YTA0ZTJkNDg5NDcyNDAzNmM1ODg0YjA3NiJ9.Be8tcW9Dy4s-IgW4kHg33uyqU22dTkDxBoOqn1TE99k&download=image.png "")

# 数组与方法的操作（难）

## 1、范例：让方法的参数接收数组

![](https://tcs.teambition.net/storage/3124def635bc6095328d044a25be9294dc65?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkZWY2MzViYzYwOTUzMjhkMDQ0YTI1YmU5Mjk0ZGM2NSJ9.c39I4Cdpn4cmTXBQgluLnZhDTGGEd9FZMae7Xf_dM5Q&download=image.png "")

![](https://tcs.teambition.net/storage/31246870c087297c9c42462acbc5b35284dc?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ2ODcwYzA4NzI5N2M5YzQyNDYyYWNiYzViMzUyODRkYyJ9.QZvPkFkWct8_DMqOmNqfy-Et885NxPpVTb7RIz5dW2U&download=image.png "")

## 2、范例：现在假设有一个int型数组，在里面有多个数据，如果要想判断某一个数据是否存在，该如何实现？

- 垃圾实现（别用）

![](https://tcs.teambition.net/storage/3124c89e8ed9fa10e14f65fdddb0929248d2?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjODllOGVkOWZhMTBlMTRmNjVmZGRkYjA5MjkyNDhkMiJ9.g2Po790-s0QzasDqpul1t47q7iQbB44ZfQ2-DqOHcQ4&download=image.png "")

- 方法实现

![](https://tcs.teambition.net/storage/3124deeaff178f956807373e132ed75ab0b6?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkZWVhZmYxNzhmOTU2ODA3MzczZTEzMmVkNzVhYjBiNiJ9.7POUuer63-DjTxtarBVsI5Jp_VTx4WNLPjzF4YtcoUw&download=image.png "")


开发原则：主方法之中的代码越少越好，主方法只需要调用方法就可以完成指定的功能。

- 利用方法减少客户端代码，在java之中有一个命名规范，如果说某一个方法返回的数据类型是boolean类型，一般此方法名称都会以 “isXxx()” 的形式命名。

## 3、范例：定义方法修改数组内容。

![](https://tcs.teambition.net/storage/3124c815df64a4c5978902930beaf70c14bb?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjODE1ZGY2NGE0YzU5Nzg5MDI5MzBiZWFmNzBjMTRiYiJ9.iKMpQ4kZHMwGJBjISmLYfr4TXAGZvD4TZ7n4xhtC_sQ&download=image.png "")

![](https://tcs.teambition.net/storage/31248b0c51f93e66e81e6ddcaacc2ebd3c2a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4YjBjNTFmOTNlNjZlODFlNmRkY2FhY2MyZWJkM2MyYSJ9.AEBgybTJvs5TuXvQ_g8it1Xd7_WwmXbIKNRpB9gOFRM&download=image.png "")

在引用数据类型操作之中，经常会出现在方法里面修改引用数据类型的形式，此时不要看代码，要回顾内存关系。

- 注意：引用数据类型之中最大的的特点是方法里面可以修改数组内容。


## 4、范例：定义方法返回数组

![](https://tcs.teambition.net/storage/312475228dc071f8baa15c3dd94974f976c2?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3NTIyOGRjMDcxZjhiYWExNWMzZGQ5NDk3NGY5NzZjMiJ9.XUA4cpTTnrDTACYC-G_by5ZxuulYRa8RvE1skKB2_Ao&download=image.png "")


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

## 5、范例：现在假设给出一个double型数组，要求定义一个方法，此方法可以统计出数组各个元素的和、平均值、最大值、最小值。

解题思路：一般一个方法只能够返回一个数据类型，但是现在需要返回的数据有四个，那么只能够将方法的返回值类型定义为数组，其中此数组第一个元素表示和，第二个元素表示平均值，第三个元素表示最大值，第四个元素表示最小值。

![](https://tcs.teambition.net/storage/31247347629a0f085b87eef8f8bc707be221?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3MzQ3NjI5YTBmMDg1Yjg3ZWVmOGY4YmM3MDdiZTIyMSJ9.voVNHEtMJaQzK2fkcxmMbWr9Gc8emTUe7_4gE3wXW3w&download=image.png "")

![](https://tcs.teambition.net/storage/31240ab7e656fcc70ac9986bf82c62d7b130?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQwYWI3ZTY1NmZjYzcwYWM5OTg2YmY4MmM2MmQ3YjEzMCJ9.2ycYjXEoaO3zGntmH0QunwoKAQ43RAL7VmGh9Rvt40U&download=image.png "")

![](https://tcs.teambition.net/storage/31244b19c46b37ef086d4d3cce4aafea0356?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ0YjE5YzQ2YjM3ZWYwODZkNGQzY2NlNGFhZmVhMDM1NiJ9.QglebNsw0F7RDk6vtm-89gcagBZDp41n93HZrASeM5g&download=image.png "")

```java
public class Ex3 {
	public static void main(String[] args) {
		int[] data = new int [] {1,2,5,4,3,9};
		int[] result = init(data);
		System.out.println(result[0]);
		System.out.println(result[1]);
		System.out.println(result[2]);
		System.out.println(result[3]);
	}
	public static int[] init(int[] arry) {
		int sum = arry[0];
		int max = arry[0];
		int min = arry[0];
		for(int i = 0;i<arry.length;i++) {
			sum += arry[i];
			if(max < arry[i]) {
				max = arry[i];
			}
			if(min > arry[i]) {
				min = arry[i];
			}
		}
		int avg = sum /arry.length;
		return new int[] {sum,max,min,avg};
	}
}
```

### 面试题：请将一个数组进行转置

1. 情况一：转置的数组是一维数组。

- 原始数组：1、2、3、4、5、6、7、8、9

- 转置数组：9、8、7、6、5、4、3、2、1

    - 方法一：定义一个新数组，而后将原始数据倒着保存到新数组之后，再去改变原始数组的引用。（尽量避免使用）

        - 此方法一定会产生垃圾空间，而产生垃圾空间的代码我们应该尽量回避。

![](https://tcs.teambition.net/storage/3124cf06f5ce495cb0b2f1ad2c343f871e05?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjZjA2ZjVjZTQ5NWNiMGIyZjFhZDJjMzQzZjg3MWUwNSJ9.Pcg8qCW9vG3--9S7mf1Xzv9_CzhQifPKJAlpT7KlA_o&download=image.png "")

    - 方法二：实现数据的首尾交换。

        - 第一种情况：数组的长度为奇数长度。

        - 第二种情况：数组的长度为偶数长度。

奇数长度：

![](https://tcs.teambition.net/storage/31242e9c289203c5feed33136ec92f1065d0?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQyZTljMjg5MjAzYzVmZWVkMzMxMzZlYzkyZjEwNjVkMCJ9.9xCLr52unT36zr8fM56INq0walLDtNoMxNnfKBl-zTw&download=image.png "")

偶数长度：

![](https://tcs.teambition.net/storage/3124a4011d9a9b18fbff87c02db36b5b53a9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRhNDAxMWQ5YTliMThmYmZmODdjMDJkYjM2YjViNTNhOSJ9.7WOIwWcM0lTx56bbSdUT5spDqXAzlYyixd5A5lk7t4k&download=image.png "")

![](https://tcs.teambition.net/storage/31247c5abadc34ca623588e8b2aefe307d5b?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3YzVhYmFkYzM0Y2E2MjM1ODhlOGIyYWVmZTMwN2Q1YiJ9.0loCYr4N8ThMLu9wDtVuiIwpyoPDwOyc6_qO1MEaowo&download=image.png "")

![](https://tcs.teambition.net/storage/312433810077486ff156ada6a61bf0af3f6a?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQzMzgxMDA3NzQ4NmZmMTU2YWRhNmE2MWJmMGFmM2Y2YSJ9.rCTi5w5C2Epse5MRxTXs7xscVUXjpzKzp3TftRYDuZQ&download=image.png "")

1. 情况二：转置的数组是二维数组。

转置前提：行和列相同

![](https://tcs.teambition.net/storage/3124a3d7e1a9bb2f55982c80f4bdc0abcbbd?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRhM2Q3ZTFhOWJiMmY1NTk4MmM4MGY0YmRjMGFiY2JiZCJ9.BDYHANF03UelJJHOCgcNnwQXBjuiEtSde8c2a7G7-3c&download=image.png "")

![](https://tcs.teambition.net/storage/3124a886b932ada1369b124aed58a9229831?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRhODg2YjkzMmFkYTEzNjliMTI0YWVkNThhOTIyOTgzMSJ9.y1IXFcd-DRmhTpfRrr6SvDPloLxxErj667mKIHAdX1Y&download=image.png "")

![](https://tcs.teambition.net/storage/312476de1c740aaea2ee4fc7cb909e44aec7?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3NmRlMWM3NDBhYWVhMmVlNGZjN2NiOTA5ZTQ0YWVjNyJ9.aOY9GxQoz7WkVzN7IKGYDffpXSVfOqIpG0_9rKaJYbw&download=image.png "")

# 与数组有关的操作方法

1、数组拷贝：

- 语法（不完整）：System.arraycopy(原数组名称，原数组开始点，目标数组名称，目标数组长度);

范例：实现数组拷贝

- 数组一：1、2、3、4、5、6、7、8、9

- 数组二：11、22、33、44、55、66、77、88、99

- 拷贝后的数组一：1、2、3、55、66、77、7、8、9

![](https://tcs.teambition.net/storage/3124d7b0f390926ada7990526ee5077fdfa5?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkN2IwZjM5MDkyNmFkYTc5OTA1MjZlZTUwNzdmZGZhNSJ9.7ulHoJL_Nm5Y5667xv0t4ZLkWNOglCGE3z4XRzUICBg&download=image.png "")


思考题：在原有数组{1，3，5，7}上，扩充数组容量为2

- 扩充容量，数组的长度永恒都是固定的，所以此时只能够开辟一个新的数组，新数组有新的长度；

- 原始数据保留，应该在新数组之中保存已有的数据，则表示将旧的数据拷贝到新数组之中。

这样不标准：

![](https://tcs.teambition.net/storage/31248f10762bbb28c8314d55ccbf206bd46d?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4ZjEwNzYyYmJiMjhjODMxNGQ1NWNjYmYyMDZiZDQ2ZCJ9.9dgFD8YuVE8Qz8bqh1V-yKIvE7ay4_4V-n9ZD51ouzk&download=image.png "")


2、数组排序：

- 语法：java.util.Arrays.sort(数组名称);

![](https://tcs.teambition.net/storage/31247ff05b5d699dc37302c6d26cdde6ded9?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3ZmYwNWI1ZDY5OWRjMzczMDJjNmQyNmNkZGU2ZGVkOSJ9.aZSUbmvFHZUMaBONY5r-0OC_aRcRwPT1QkjlDouV1yc&download=image.png "")


# 对象数组（重点）

对象数组包含的一定是多个操作对象。

![](https://tcs.teambition.net/storage/3124c42c3bcbf662eb5bf6a47d667e70ecc1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjNDJjM2JjYmY2NjJlYjViZjZhNDdkNjY3ZTcwZWNjMSJ9.0Et8nM9nR5-Ea9G7nSO-shMfvvogybL3ZNKTLuq_OWE&download=image.png "")

范例：动态数组初始化

![](https://tcs.teambition.net/storage/3124cf120001c4423513a591e2f2ac25a5a0?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRjZjEyMDAwMWM0NDIzNTEzYTU5MWUyZjJhYzI1YTVhMCJ9.NU9mHhKr2tlutm9YqKGC-N6EpicaJ1UGTNm0nu3ulSw&download=image.png "")

![](https://tcs.teambition.net/storage/31245ee144aa239952a7eca725decf8f01dc?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ1ZWUxNDRhYTIzOTk1MmE3ZWNhNzI1ZGVjZjhmMDFkYyJ9.w2rvAodyJS441BuTNI5OrxUuN7HTOlhc21fzMzyqzy0&download=image.png "")

范例：静态数组初始化

写法一：

![](https://tcs.teambition.net/storage/3124d8fc4bdd5b05207f3de5bf70684bbf25?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjRkOGZjNGJkZDViMDUyMDdmM2RlNWJmNzA2ODRiYmYyNSJ9.cIAk-FGihVU4vQA1axirqQgg9bs69ucTroJj3bPgYJ0&download=image.png "")

写法二：

![](https://tcs.teambition.net/storage/31248866efae613ba68713d90de41d85a845?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ4ODY2ZWZhZTYxM2JhNjg3MTNkOTBkZTQxZDg1YTg0NSJ9.19mnbyXBgOtFx8b1mpdKH5oBHXQxB9CAh70oJpf1LP4&download=image.png "")

# 总结：

![](https://tcs.teambition.net/storage/31247c2a884269adac6e27db00bde6ed953e?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3YzJhODg0MjY5YWRhYzZlMjdkYjAwYmRlNmVkOTUzZSJ9._uJQJpxrlStRbZZmg1LFCwMM_D_nWIZ6o60nAvx3MTk&download=image.png "")

![](https://tcs.teambition.net/storage/31247e951f30b28e5a615b2a3fd93213b8f1?Signature=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJBcHBJRCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9hcHBJZCI6IjU5Mzc3MGZmODM5NjMyMDAyZTAzNThmMSIsIl9vcmdhbml6YXRpb25JZCI6IiIsImV4cCI6MTYyMjAyOTQyMywiaWF0IjoxNjIxNDI0NjIzLCJyZXNvdXJjZSI6Ii9zdG9yYWdlLzMxMjQ3ZTk1MWYzMGIyOGU1YTYxNWIyYTNmZDkzMjEzYjhmMSJ9.m2nh1SEynY4k2YtMeGbSURVnWRDcFM8Ky4321UCxSFE&download=image.png "")

