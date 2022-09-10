---
date : 2022-09-10
title : "[Java] Java String Method Basic"
comments : true
categories : 
    - Java
---

```java
public class Main
{
	public static void main(String[] args) {
// 		String str = new String("Hello");
		String str = "Hello";
		System.out.println(str.length());
		System.out.println(str.concat("World!"));
		System.out.println(str.substring(2,3));
		
	}
}

```